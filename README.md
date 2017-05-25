As per documentation:

http://docs.grails.org/3.3.x/guide/conf.html#multipleDatasources


configuration added and upon start:

```groovy
2017-05-25 17:30:59.919 ERROR --- [           main] o.s.boot.SpringApplication               : Application startup failed

org.springframework.beans.factory.BeanExpressionException: Expression parsing failed; nested exception is org.springframework.expression.spel.SpelEvaluationException: EL1007E: Property or field 'dataSource' cannot be found on null
        at org.springframework.context.expression.StandardBeanExpressionResolver.evaluate(StandardBeanExpressionResolver.java:164)
        at org.springframework.beans.factory.support.AbstractBeanFactory.evaluateBeanDefinitionString(AbstractBeanFactory.java:1448)
        at org.springframework.beans.factory.support.BeanDefinitionValueResolver.doEvaluate(BeanDefinitionValueResolver.java:255)
        at org.springframework.beans.factory.support.BeanDefinitionValueResolver.evaluate(BeanDefinitionValueResolver.java:228)
        at org.springframework.beans.factory.support.BeanDefinitionValueResolver.resolveValueIfNecessary(BeanDefinitionValueResolver.java:204)
        at org.springframework.beans.factory.support.ConstructorResolver.resolveConstructorArguments(ConstructorResolver.java:648)
        at org.springframework.beans.factory.support.ConstructorResolver.autowireConstructor(ConstructorResolver.java:145)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.autowireConstructor(AbstractAutowireCapableBeanFactory.java:1193)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1095)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:513)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:483)
        at org.springframework.beans.factory.support.AbstractBeanFactory$1.getObject(AbstractBeanFactory.java:306)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:230)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:197)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.preInstantiateSingletons(DefaultListableBeanFactory.java:761)
        at org.springframework.context.support.AbstractApplicationContext.finishBeanFactoryInitialization(AbstractApplicationContext.java:866)
        at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:542)
        at org.springframework.boot.context.embedded.EmbeddedWebApplicationContext.refresh(EmbeddedWebApplicationContext.java:122)
        at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:737)
        at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:370)
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:314)
        at grails.boot.GrailsApp.run(GrailsApp.groovy:83)
        at grails.boot.GrailsApp.run(GrailsApp.groovy:388)
        at grails.boot.GrailsApp.run(GrailsApp.groovy:375)
        at grails.boot.GrailsApp$run.call(Unknown Source)
        at org.codehaus.groovy.runtime.callsite.CallSiteArray.defaultCall(CallSiteArray.java:48)
        at org.codehaus.groovy.runtime.callsite.AbstractCallSite.call(AbstractCallSite.java:113)
        at org.codehaus.groovy.runtime.callsite.AbstractCallSite.call(AbstractCallSite.java:133)
        at test330.Application.main(Application.groovy:8)
Caused by: org.springframework.expression.spel.SpelEvaluationException: EL1007E: Property or field 'dataSource' cannot be found on null
        at org.springframework.expression.spel.ast.PropertyOrFieldReference.readProperty(PropertyOrFieldReference.java:220)
        at org.springframework.expression.spel.ast.PropertyOrFieldReference.getValueInternal(PropertyOrFieldReference.java:94)
        at org.springframework.expression.spel.ast.PropertyOrFieldReference.access$000(PropertyOrFieldReference.java:46)
        at org.springframework.expression.spel.ast.PropertyOrFieldReference$AccessorLValue.getValue(PropertyOrFieldReference.java:375)
        at org.springframework.expression.spel.ast.CompoundExpression.getValueInternal(CompoundExpression.java:88)
        at org.springframework.expression.spel.ast.SpelNodeImpl.getValue(SpelNodeImpl.java:120)
        at org.springframework.expression.spel.standard.SpelExpression.getValue(SpelExpression.java:242)
        at org.springframework.context.expression.StandardBeanExpressionResolver.evaluate(StandardBeanExpressionResolver.java:161)
        ... 29 common frames omitted


FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':bootRun'.
> Process 'command '/usr/lib/jvm/jdk1.8.0_45/bin/java'' finished with non-zero exit value 1

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output.
| Error Failed to start server (Use --stacktrace to see the full trace)


```
