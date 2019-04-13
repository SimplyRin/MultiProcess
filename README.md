# MultiProcess
Thread を使いやすく

マルチスレッドで複数の処理を実行させ、終了時指定した処理を実行することができる

# Sample
```Java
MultiProcess multiProcess = new MultiProcess();

// 処理するスレッドを追加
multiProcess.addProcess(() -> {
});

// 上記で追加した処理がすべて終了したときに実行されるコード
multiProcess.setFinishedTask(() -> {
});

// 最大処理数 (多ければ多いほど処理速度は向上しますが、PCが不安定になる場合があります)
multiProcess.updateMaxThread(1024);

// 上記の内容で処理を開始
multiProcess.start();
```

# License
- [Apache-2.0](https://github.com/SimplyRin/MultiProcess/blob/master/LICENSE.md)

# Maven
- Repository
```XML
  <repositories>
    <repository>
      <id>net.simplyrin</id>
      <name>maven-repository</name>
      <url>https://api.simplyrin.net/maven/</url>
    </repository>
  </repositories>
```

- Dependency
```XML
  <dependencies>
    <dependency>
      <groupId>net.simplyrin.multiprocess</groupId>
      <artifactId>MultiProcess</artifactId>
      <version>1.0</version>
    </dependency>
  </dependencies>
```
