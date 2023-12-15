[![Build Status](https://travis-ci.com/connectbot/connectbot.svg?branch=master)](
https://travis-ci.com/connectbot/connectbot)

# ConnectBot

ConnectBot is a [Secure Shell](https://en.wikipedia.org/wiki/Secure_Shell)
client for Android that lets you connect to remote servers over a
cryptographically secure link.


## Google Play

[![Get it on Google Play][2]][1]

  [1]: https://play.google.com/store/apps/details?id=org.connectbot
  [2]: https://developer.android.com/images/brand/en_generic_rgb_wo_60.png


## Compiling

### Android Studio

ConnectBot is most easily developed in [Android Studio](
https://developer.android.com/studio/). You can import this project
directly from its project creation screen by importing from the GitHub URL.

### Command line

To compile ConnectBot using `gradlew`, you must first specify where your
Android SDK is via the `ANDROID_SDK_HOME` environment variable. Then
you can invoke the Gradle wrapper to build:

```sh
./gradlew build
```

### Reproducing Continuous Integration (CI) builds locally

To run the Jenkins CI pipeline locally, you can use
`jenkinsfile-runner` via a Docker installation which can be invoked like
this:

```sh
docker run -it -v $(pwd):/workspace \
    -v jenkinsfile-runner-cache:/var/jenkinsfile-runner-cache \
    -v jenkinsfile-runner:/var/jenkinsfile-runner \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v $(which docker):$(which docker) \
    -e ANDROID_ADB_SERVER_ADDRESS=host.docker.internal \
    jenkins/jenkinsfile-runner
```


## Translations

If you'd like to correct or contribute new translations to ConnectBot,
then head on over to [ConnectBot's translations project](
https://translations.launchpad.net/connectbot/trunk/+pots/fortune)

经济效率是指在一定的资源条件下，实现某一目标所需的最小资源投入或者在一定的资源投入下，实现某一目标的最大化程度。经济效率是衡量项目管理系统改进方案是否合理和可行的重要指标，它反映了改进方案的成本效益比，即改进方案所带来的收益是否大于或等于所投入的成本。经济效率的计算方法有多种，本文主要采用以下三种方法：

- **投资回报率（ROI）**：投资回报率是指改进方案的净收益与总成本的比值，它反映了改进方案的盈利能力，即每投入一元成本，能够带来多少元的收益。投资回报率的计算公式为：
  $$
  ROI = \frac{\text{净收益}}{\text{总成本}}
  $$

- **净现值（NPV）**：净现值是指改进方案在一定的折现率下，未来各期的净收益的现值之和，减去初始投资的现值，它反映了改进方案的净贡献，即改进方案能够为投资者创造多少净收入。净现值的计算公式为：
  $$
  NPV = -C_0 + \sum_{t=1}^{n} \frac{C_t}{(1+r)^t}
  $$
  其中，\(C_0\) 是初始投资的现值，\(C_t\) 是第 \(t\) 期的净收益，\(r\) 是折现率，\(n\) 是改进方案的期限。

- **内部收益率（IRR）**：内部收益率是指使改进方案的净现值等于零的折现率，它反映了改进方案的收益率，即改进方案的投资与收益相等时的年化利率。内部收益率的计算方法为：找到满足以下等式的 \(IRR\)：
  $$
  C_0 + \sum_{t=1}^{n} \frac{C_t}{(1+IRR)^t} = 0
  $$
  其中，\(C_0\)，\(C_t\)，\(n\) 的含义同上。

根据以上三种经济效率的计算方法，本文将分别计算改进华为IT项目管理系统的投资回报率、净现值和内部收益率，并根据一定的标准，评估改进方案的经济效率水平。希望这些信息对您有所帮助！
