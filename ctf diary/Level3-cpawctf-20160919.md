#Level3-cpawctf
計算・SQLi・復元  

## 解いた流れ
### Q23.[Reversing]またやらかした！
Q21と同じようにとりあえず実行してみたら残念ながら何にも出てこなかったし、strngsコマンドをしてもそれらしいものは出てこなかった。  
前回参考にしたサイト見ると解析は「gdb」を使うみたい。逆アセンブリっていうのをするみたい。  
見よう見まねで一度rev100のほうでやってどこにflagが書かれているか確認した。でもrev200でうまくいかなかった。  
どうやらブレークポイントなるものをするみたい…。でもどこを壊せばいいかわからなくてなんとなくDWORDが終わった部分とかにやってみたり最後のほうかたっぱしにやってみた。  
でそんなこんなで終了。なんか最後の方だいぶテキトーにやってた…。いかんね。  
＜参考＞<http://www.k3.dion.ne.jp/~dt2/usamimihurricane/webhelp/_RESOURCE/words/words6A.html>  
＜参考＞<http://itpro.nikkeibp.co.jp/members/ITPro/ITBASIC/20021220/1/>  
＜参考＞<http://wiki.bit-hive.com/north/pg/%A5%B3%A5%DE%A5%F3%A5%C9%B0%FA%BF%F4%A4%C8%B4%C4%B6%AD%CA%D1%BF%F4>  
＜参考＞<http://inaz2.hatenablog.com/entry/2014/05/03/044943>  

### Q24.[Web]Baby's SQLi - Stage 2-
「Q22.[Web]Baby's SQLi - Stage 1-」を解いたときにFlagと一緒に出てきたアドレスに飛ぶ。  
パスワードがわからないから、とりあえず「’＃」で済ませようとしたら下も入力しろって怒られた。  
んじゃ、or文の方かってことで「' OR 'A' = 'A」って打って終了。  
※ctf4gでちゃんと文法を習ったわけではないから使えない記号がわからなくて困った。ちゃんと習いたい…。  

### Q26.[PPC]Remainder theorem
とりあえずコード書いて計算してもらった。どうやら、int型は32ビットで9桁までしか計算できないらしい…。  
そのせいでエラー出たから、いろいろ調べて「unsigned long long int」使って何とか出来た！  
＜参考＞<http://seclan.dll.jp/c99d/c99d05.htm>  
＜参考＞<https://github.com/wmrn/ctf_for_myself/blob/master/cpaw_q26.c>  

### Q29.[Crypto] Common World
計算するだけなのは知ってるけどこの桁数対応してる言語に慣れてないから疲れてあきらめた。  

## ちょっとしたポイント
--ほかの問題とかにも使えそうなポイントの説明--
 
## 最後に
* ハリネズミ本を一通り読みたいと思った。2016/09/19
