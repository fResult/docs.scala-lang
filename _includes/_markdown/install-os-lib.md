{% altDetails require-info-box 'Getting OS-Lib' %}

{% tabs oslib-install class=tabs-build-tool %}
{% tab 'Scala CLI' %}
You can require the entire toolkit in a single line:
```scala
//> using toolkit latest
```

Alternatively, you can require just a specific version of OS-Lib:
```scala
//> using dep com.lihaoyi::os-lib:0.11.3
```
{% endtab %}
{% tab 'sbt' %}
In your `build.sbt`, you can add a dependency on the toolkit:
```scala
lazy val example = project.in(file("."))
  .settings(
    scalaVersion := "3.4.2",
    libraryDependencies += "org.scala-lang" %% "toolkit" % "0.7.0"
  )
```
Alternatively, you can require just a specific version of OS-Lib:
```scala
libraryDependencies += "com.lihaoyi" %% "os-lib" % "0.11.3"
```
{% endtab %}
{% tab 'Mill' %}
In your `build.sc` file, you can add a dependency on the Toolkit:
```scala
object example extends ScalaModule {
  def scalaVersion = "3.4.2"
  def ivyDeps =
    Agg(
      ivy"org.scala-lang::toolkit:0.7.0"
    )
}
```
Alternatively, you can require just a specific version of OS-Lib:
```scala
ivy"com.lihaoyi::os-lib:0.11.3"
```
{% endtab %}
{% endtabs %}
{% endaltDetails %}
