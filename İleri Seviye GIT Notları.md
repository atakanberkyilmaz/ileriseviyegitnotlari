İleri Seviye GIT Notları
DERS-2
"Master1 | Başlık eklendi"
Commitleri bu şekilde yapabilirsin. Düzenli olsun diye. Böylece merge edilirse hangi commit hangi branchten geldi anlaşılır.



git commit --amend
Bu şekilde yeni commit atmadan mevcut commiti düzenleyebilirsin.



git revert 2f22b3a8623
Commiti silmek.



git reset --hard 8623f22b3a
Tehlikeli. Geride commit bırakmadan silmek.



git diff 66cf76ef..8623f22 index.md
Farkları gösterir.



DERS-3
git branch header
Header adında bir branch açar.



git chechout header
Headera geçer.



git checkout -b footer
Hem oluşturur hem geçer.



git branch -D footer
Siler.



git stash
Stashe alır. Değişiklikler geri alınır. Son committeki haline döner ama. Değişiklikler stahste.



git stash list
Stashe alınan şeyleri listeler.



git stash clear
Stahi siler.



git stash pop
En üstteki kaydı getirir. Stashte bişey kalmaz ama. Ordan da kaldırır.



git stash apply stash@{0}
Stashtekini getir ama kaldırma orda dursun.



DERS-4
git merge header
Zaten masterdayız headerı mastera merge et.



git merge --squash footer
Bütün commitleri birleştirmeden merge ediyor. En son senin bir commit daha atman gerek. Böylece bu committe merge edildiğini belirtebilirsin. Okuyan nerde merge edildiğini anlayabilsin diye. Ayrıca diğer branchteki tüm commitleri de getirmemiş olursun. Tek commit gözükür. Böylece logu çorba etmemiş oluruz.



git rebase header
Headeri alır ama ortada bir merge yok sadece aldı.



Merge ederken çakışırsa conflict olur. Conflict'ten kurtulmak için merge işlemini şöyle geri alabilirsin.

git merge --abort