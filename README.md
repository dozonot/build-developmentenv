# ansible-os-setup

## このリポジトリについて

このリポジトリはインフラ勉強会で開催された「Ubuntuの開発環境構築を手伝って！」用のリポジトリです。
Ref: [Google Slide](https://docs.google.com/presentation/d/1J-izPPRO2L8ktKaEguczFNBYPEy46JR9V2rV9g4hh-k/edit?usp=sharing)

利用は自己責任でお願いいたします。

## 使い方

Ubuntu OSのインストールが終了したら次のコマンドを実行します。

```
sudo apt update && sudo apt upgrade && sudo apt install -y ansible python
git clone https://github.com/dozonot/build-devenv.git
cd build-devenv
sudo cp config/sudoers /etc/sudoers; sudo chown root.root /etc/sudoers; sudo chmod 440 /etc/sudoers
ansible-playbook -i localhost, -c local playbook.yml
sudo reboot
```
