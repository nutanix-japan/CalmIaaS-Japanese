.. _calm_enable:

------------
Calm: 有効化
------------

概要
++++++++

.. note::

  本演習のステップは多くの場合、既に実施済みの内容となります。インストラクターから指示のあった場合のみ、行って下さい。

  完了までの概算時間: **10分**

この演習では、Nutanix Calmを有効化します。

アプリケーション管理を有効にする
+++++++++++++++++++++++

CalmはPrism Centralに組み込まれているため、管理するための追加のアプライアンスやコンソールは必要ありません。Calmを使用して環境内のアプリケーションの管理を開始するには、サービスを有効にする必要があります。

.. note::

  Calm は、Prism Centralインスタンスごとに1回のみ有効にすることができます。 もし **アプリ管理の有効化** が緑色のチェックマークを表示している場合は、使用しているPrism CentralインスタンスでCalmがすでに有効になっていることを意味します。 **そうであれば、本演習は不要です。**

#. **Prism Central** で、 **?** ドロップダウンメニューをクリックし、 **Prism Centralの新規** を展開し、 **アプリ管理を有効にする** を選択します。

#. **有効化** をクリックします。

   .. figure:: images/5.10/enable1.png

#. **アプリ管理を有効にする** を選択し、 **保存** をクリックします。

   .. note:: Nutanix Calmは、Acropolis Starter、Pro、またはUltimateエディションで使用できる個別ライセンス製品です。

   .. figure:: images/5.10/enable2.png

#. Calmが有効になっているかどうかの検証を受ける必要がありますが、これには5分から10分ほどかかります。

   .. figure:: images/5.10/enable3.png

Active Directoryの追加
+++++++++++++++++++++++

Calmが有効になるのを待っている間に、Active Directoryサーバーを追加します。 これは基本的なCarmの利用には必要ないのですが、ロールベースのアクセス制御を行う際には必要になるので、設定しておくと良いでしょう。

#. **ギアアイコン** をクリックし、 **認証** のメニューに進みます。

   .. figure:: images/5.10/enable4.png

#. ポップアップメニューで **新規ディレクトリ** をクリックします。

   .. figure:: images/5.10/enable5.png

#. 次のフィールドを記載し、 **保存** をクリックします。

   - **ディレクトリタイプ** - Active Directory
   - **名前** - NTNXLAB
   - **ドメイン** - ntnxlab.local
   - **ディレクトリURL** - ldaps://*<DC-VM-IP>*
   - **検索タイプ** - Non Recursive
   - **サービスアカウントユーザ名** - Administrator@ntnxlab.local
   - **サービスアカウントパスワード** - nutanix/4u

   .. figure:: images/5.10/enable6.png

#. ブラウザを更新し、ナビゲーションバーから **Calm** を選択します。Calmがまだ有効になっている場合は、もう1分待ってからもう一度試してみてください。
