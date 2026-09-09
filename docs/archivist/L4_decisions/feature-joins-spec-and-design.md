# spec と design の整合を担保するのは feature だけ

L2 の二つが互いを引かない以上、突き合わせられる場所は上の層にしかない。それは
feature 一つに限る。

覆しにくい決定。

feature は availability ごとに spec と design を並べた表を持つ。行に空欄があれば、
約束したが解いていないか、作ったが約束していないかのどちらかになる。どちらも
不備として出荷を止める。実装に入る前に、spec の甘さか design の甘さがそこに出る。

feature が下層の要約でないことは変わらない。表の主キーは決断から起こした
availability であり、spec と design はその行に集まる従属列になる。この表が入って
はじめて、feature は design の写像でなくなる。
