---
title: InfoPath にカスタム機能を追加する COM アドインを作成します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007 では、com アドインを作成する InfoPath 2007 では、独自の機能では、COM アドインが [InfoPath 2007] を追加します。
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath には、ユーザー エクスペリエンスの編集フォームを拡張するための COM アドインがサポートされています。 COM アドインが最初に追加した InfoPath では、他の Office アプリケーションなど、Microsoft Office Word と Microsoft Office Excel サポートされている COM アドインが Office 2000 以降をサポートします。
ms.openlocfilehash: 4c70dfb71cf7b15a0978b4567ffac02a8ba524c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799013"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>InfoPath にカスタム機能を追加する COM アドインを作成します。

Microsoft InfoPath には、ユーザー エクスペリエンスの編集フォームを拡張するための COM アドインがサポートされています。 COM アドインが最初に追加した InfoPath では、他の Office アプリケーションなど、Microsoft Office Word と Microsoft Office Excel サポートされている COM アドインが Office 2000 以降をサポートします。
  
InfoPath での COM アドイン サポートはフォーム編集環境用に使用できます。COM アドインを使用してもフォーム デザイン環境は拡張できません。
  
## <a name="the-idtextensibility2-interface"></a>IDTExtensibility2 インターフェイス

イベントとして機能する 5 つのメソッドを提供するデュアル インターフェイス オブジェクトは、InfoPath 編集環境では、 **IDTExtensibility2**インターフェイスは、COM アドインの**IDTExtensibility2**の開発者が実装する必要があるサポートが用意されています編集環境です。 これらのメソッドは、次の表に記載されている、スタートアップとシャット ダウンの条件を環境に対応する COM アドインを使用できます。 
  
|**インターフェイス**|**説明**|
|:-----|:-----|
|**OnAddInsUpdate (バリアントとして ByVal custom())** <br/> |環境内でのアドインの読み込み時、またはアンロード時に発生します。  <br/> |
|**OnBeginShutdown (バリアントとして ByVal custom())** <br/> |環境のシャット ダウン中に発生します。  <br/> |
|**OnConnection (ByVal アプリケーションのオブジェクトとして、ByVal ConnectMode として ext_ConnectMode、ByVal AddInInst のオブジェクトとして、ByVal custom() バリアントとして)** <br/> |アドインが環境に読み込まれると発生します。  <br/> |
|**OnDisconnection (ByVal の RemoveMode と ext_DisconnectMode、ByVal custom() のバリアントとして)** <br/> |アドインが環境からアンロードされると発生します。  <br/> |
|**OnStartupComplete (バリアントとして ByVal custom())** <br/> |環境の起動が完了すると発生します。  <br/> |
   
## <a name="registering-com-add-ins"></a>COM アドインの登録

InfoPath を含め、すべての Office アプリケーションはレジストリを使用して、COM アドイン コレクション内のアドインの一覧表示、接続状態の格納、ブートやデマンド読み込み情報の格納を行います。InfoPath COM アドインの場合、次のキーの下に、各アドインの名前が表示されます。
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
クライアント コンピューターのすべてのユーザーが使用できる COM アドインがインストールされている場合は、HKLM レジストリ ハイブにレジストリ キーがあります。
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
レジストリ キーの名前は、アドインの**ProgIdAttribute**に対応して、次の値が含まれています。 
  
|**名前**|**型**|**説明**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**文字列型 (String)** <br/> |**[COM アドイン**] ダイアログ ボックスに表示され、**セキュリティ センター**の **[アドイン**] ページに表示される名前。  <br/> |
|**説明** <br/> |**String** <br/> |アドインが**セキュリティ センター**で選択したときに表示される文字列です。  <br/> |
|**LoadBehavior** <br/> |**DWORD** <br/> |COM アドインの読み込み方法を指定します。値は 0、1、2、8、および 16 を組み合わせたものです。詳細については、次の表を参照してください。  <br/> |
   
**LoadBehavior**の**DWORD**値は、編集環境に COM アドインをロードするか方法を示す値を含める必要があります。 以下のテーブルまたはテーブルからの値の組み合わせを指定できます。 たとえば、COM アドインを作成した Visual Studio 2005 では「3」が読み込まれているは、 **LoadBehavior**アプリケーションの起動時に、接続されています。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |切断します。 アドインには、 **COM アドイン**] ダイアログの [非アクティブとして表示されます。  <br/> |
|1  <br/> |接続されています。 アドインには、アクティブで、[ **COM アドイン**] ダイアログ ボックスとして表示されます。  <br/> |
|2  <br/> |起動時に読み込む。アドインは、ホスト アプリケーションの起動時に読み込まれ、接続されます。  <br/> |
|8  <br/> |必要時に読み込む。アドインは、ユーザーがアドインの機能を使用するボタンをクリックした時など、ホスト アプリケーションが要求した場合に読み込まれ、接続されます。  <br/> |
|16  <br/> |初回に接続する。アドインを登録した後にユーザーがホスト アプリケーションを実行した時に、アドインは初めて読み込まれます。  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Visual Studio 2005 または Visual Studio 2008 を利用したマネージ COM アドインの作成

Microsoft Visual Studio 2005 または Visual Studio 2008 を使用してマネージ COM アドインを作成するには、次の手順で共有アドイン プロジェクトを作成します。  
  
1. Visual Studio を起動します。
    
2. [**ファイル**] メニューの [**新しいプロジェクト**] をクリックします。
    
3. **[新しいプロジェクト**] ダイアログ ボックスの [**プロジェクトの種類**] ペインで**その他のプロジェクトの種類**] フォルダーをクリックし、[**機能拡張**] をクリックします。
    
4. **[テンプレート**] ペインで、[**共有アドイン**] をクリックします。
    
5. **[名前**] ボックスで、プロジェクトの名前を入力します。 
    
6. **[場所**] ボックスでフォルダー パスを入力または [**参照**] をクリックしてフォルダー パスを選択し、し、[ **OK**] をクリックします。 **共有アドイン ウィザード**が表示されます。 
    
7. **次**の**共有アドイン ウィザード**でをクリックします。 **プログラミング言語の選択**] ページが表示されます。 
    
8. **Visual Basic を使用してアドインを作成**するには、をクリックし、[**次へ**] をクリックします。 **アプリケーション ホストの選択**ページが表示されます。 
    
9. **Microsoft InfoPath**以外には、各アプリケーションの横にあるボックスをオフにし、[**次へ**] をクリックします。 **名前を入力し説明**のページが表示されます。 
    
10. **アドインの名前**] ボックスに、COM アドインの名前を入力します。 
    
11. **アドインの説明**] ボックスに、COM アドインの説明を入力し、[**次へ**] をクリックします。 **アドイン オプションの選択]** ページが表示されます。 
    
12. **マイ アドインをホスト アプリケーションの読み込み時にロードすると思い**、ボックスの **[アドインをそれをインストールしたユーザーだけでなく上にインストールされているコンピューターのすべてのユーザーに利用可能にする必要があります**を確認します。 
    
13. [**次へ**、[**概要**] ページを確認する] をクリックし、[**完了**] をクリックします。
    
Visual Studio でプロジェクトの作成後は、2 つのプロジェクトがソリューション エクスプ ローラー] ウィンドウが表示されます。 最初のプロジェクトは、プロジェクトの COM アドインです。2 番目のプロジェクトは、COM アドインを展開するためのセットアップ プロジェクトです。 **共有アドイン ウィザード**は次の手順を使用して InfoPath オブジェクト ライブラリへの参照を挿入する必要があるためだけ、 **Microsoft Office の 14.0 オブジェクト ライブラリ**への参照を挿入します。
  
1. アドイン プロジェクトのプロパティを表示するのには **[My Project** ] をダブルクリックします。 プロジェクトに自動的に追加された参照を表示するのには [**参照設定**] タブをクリックします。 
    
2. **参照の追加**] ダイアログ ボックスを表示するのには [**追加**] ボタンをクリックします。 
    
3. [ **COM** ] タブでは、 **Microsoft.InfoPath 2.0 のタイプ ライブラリ**をダブルクリックし、[ **OK**] をクリックします。
    
4. **Microsoft InfoPath 3.0 のタイプ ライブラリ**への参照を追加することも削除する必要のある 3 つのアセンブリへの参照を追加: **ADODB** **MSHTML**、 **MSXML2**です。 **参照**[**ソリューション エクスプ ローラー**でこれらの参照をそれぞれ右クリックし、[**削除**] をクリックします。
    
## <a name="viewing-the-registry-settings"></a>レジストリ設定の表示

COM アドインのインストール時に作成されるレジストリ設定を表示するには、以下の手順を実行します。
  
1. **ソリューション エクスプ ローラー**でセットアップ プロジェクトのルート ノードを右クリックし、**ビュー**、[**エディター**] をクリックし、[**レジストリ**] をクリックします。
    
2. 左側ペインで、 **HKEY_LOCAL_MACHINE**、**ソフトウェア**、**マイクロソフト**、 **InfoPath**では、し、**アドイン**を展開するをクリックします。
    
3. 共有アドイン プロジェクトの**ProgID**に対応する名前をクリックします。
    
これらのプロパティを変更するにプロパティを右クリックし **[プロパティ] ウィンドウ**で、 **[プロパティ] ウィンドウ**の [**値**] ボックスを変更します。
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>共有アドインのコンパイルと配布

共有アドイン プロジェクトが開発されたコンピューターでテストするためにマネージ COM アドインをコンパイルするには、ソリューション エクスプローラーで共有アドイン プロジェクトのルート ノードを右クリックし、[ビルド] をクリックします。エラーが出ずにプロジェクトがビルドすると、InfoPath 編集環境を起動し、マネージ COM アドインの使用を開始できます。実行中の InfoPath のインスタンスがある場合は、プロジェクトをビルドする前に閉じてください。COM アドインが登録されていることを確認するために、[COM アドイン] ダイアログ ボックスを開く必要がある場合があります。[COM アドイン] ダイアログ ボックスは、次の手順で開きます。
  
1. InfoPath 編集環境を開く最も簡単な方法は、既存のフォーム テンプレートを開きます。すると、そのフォーム テンプレートに基づいて新しいフォームが作成されます。
    
2. [**ツール**] メニューには、**セキュリティ センター**をクリックします。 
    
3. 左側の [**アドイン**] カテゴリをクリックします。 
    
4. [**管理**] セクションで、[**セキュリティ センター** ] ダイアログ ボックスの下部にあるリストから **[COM アドイン]** を選択し、 **[移動**] ボタンをクリックします。 
    
5. [ **COM アドイン**] ダイアログ ボックスで、最近ビルドしたアドインの名前が表示され、その横にあるチェック ボックスが存在する必要があります。 横のチェック ボックスがない場合、COM アドインの読み込みに失敗しました] ダイアログ ボックスの **[ロード方法**] セクションに表示されるエラーが発生したためです。 
    
共有アドイン プロジェクトが開発されたコンピューター以外のコンピューターで使用するマネージ COM アドインをコンパイルするには、次の追加手順に従ってコードをセキュリティで保護してください。他のコンピューターで使用する共有アドイン プロジェクトをセキュリティで保護する方法については、次の 3 つの資料を参照してください。
  
- [マネージ COM アドインが Office XP での展開](http://go.microsoft.com/fwlink/?LinkID=73473)
  
- [COM アドイン Shim ソリューションを使用してマネージ COM アドインで Office XP を展開するには](http://go.microsoft.com/fwlink/?LinkID=73474)
  
- [COM シム ウィザードを使用して Office 拡張機能を分離します。](http://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> COM アドインを分離していない場合、メモリ リークが発生し、アプリケーションが不安定になる可能性があります。 
  
> [!NOTE]
> .NET Framework または設定プロジェクトが要求するその他の必要なアセンブリがターゲット コンピューターにインストールされていないと、.msi ファイルが正しくインストールされない可能性があります。また、.msi ファイルを配布するだけで .msi ファイルをインストールすることはできません。Visual Studio によって生成された元の .msi ファイルと同じフォルダー内の他のサポート ファイルも配布する必要があります。 
  
## <a name="coding-in-the-com-add-in"></a>COM アドインでのコーディング

InfoPath のフォーム編集環境で発生したアプリケーション イベントは、COM アドインでキャプチャできます。 [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx)オブジェクトの次のイベントは、ユーザー アクションに応答するのには COM アドインによって使用できます。 
  
|**�C�x���g**|**���**|
|:-----|:-----|
|[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx)イベント  <br/> |新しいフォームが作成されるときに発生します。  <br/> |
|[終了](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx)イベント  <br/> |ユーザーが InfoPath を終了するときに発生します。  <br/> |
|[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx)イベント  <br/> |任意の文書ウィンドウがアクティブになるときに発生します。  <br/> |
|[ただし](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx)イベント  <br/> |任意の文書ウィンドウが非アクティブになったときに発生します。  <br/> |
|[WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx)イベント  <br/> |ドキュメント ウィンドウのサイズが変更されるとき、または移動されるときに発生します。  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx)イベント  <br/> |開いている文書が閉じる直前に発生します。  <br/> |
|[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx)イベント  <br/> |開かれているドキュメントが印刷される直前に発生します。  <br/> |
|[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx)イベント  <br/> |開かれているドキュメントが保存される直前に発生します。  <br/> |
|[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx)イベント  <br/> |新しいフォームが作成されるとき、既存のフォームが開かれるとき、または別のフォームがアクティブになるときに発生します。  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx)イベント  <br/> |文書が開いたときに発生します。  <br/> |
   
COM アドインでこれらのイベントをキャプチャするには、 **Connect**クラスに次のクラス レベル変数を宣言する必要があります。 
  
```vb
InfoPathApplication = DirectCast( _
   application, Microsoft.Office.Interop.InfoPath._Application3)
InfoPathApplicationEvents = DirectCast( _
   InfoPathApplication.Events, _
   Microsoft.Office.Interop.InfoPath.ApplicationEvents)
```

```cs
InfoPathApplication =
   (Microsoft.Office.Interop.InfoPath._Application3)application;
InfoPathApplicationEvents =
   (Microsoft.Office.Interop.InfoPath.ApplicationEvents)
   InfoPathApplication.Events;
```

[_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx)オブジェクトをアドインで、**オブジェクト**が受信した汎用アプリケーションを最初の行にキャストします。 2 行目は、 **_Application3**オブジェクト ( **InfoPathApplication**変数によって表されます) の[イベント](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx)のプロパティを[ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx)オブジェクトにキャストします。 
  
イベント ハンドラーを作成するには、 **InfoPathApplicationEvents**を Visual Studio ウィンドウの上部にある [**クラス名**] ドロップダウン ボックスから選択し、ビジュアルの上部にある [**メソッド名**] ボックスで処理するイベントを選択し、Studio ウィンドウです。 たとえば、フォームの保存時に制御する場合は、 **XDocumentBeforeSave**イベントを処理します。 **メソッド名**] ボックスの一覧から**XDocumentBeforeSave**を選択すると、自動的に次の手順を挿入します。 
  
```vb
Private Sub InfoPathApplicationEvents_XDocumentBeforeSave( _
   ByVal pDocument As Microsoft.Office.Interop.InfoPath._XDocument, _
   ByRef pfCancel As Boolean) _
   Handles InfoPathApplicationEvents.XDocumentBeforeSave
End Sub
```

```cs
private void InfoPathApplicationEvents_XDocumentBeforeSave(
   Microsoft.Office.Interop.InfoPath._XDocument pDocument, ref bool pfCancel)
{
}

```

**ApplicationEvents**オブジェクトのイベントのいずれかによって、COM アドインの同じメソッドを使用して処理できます。 
  
## <a name="see-also"></a>関連項目

- [Microsoft Office 2000 COM アドインを作成します。](http://go.microsoft.com/fwlink/?LinkID=73468) 
- [マネージ COM アドインが Visual Studio .NET での Office を作成します。](http://go.microsoft.com/fwlink/?LinkID=73470)
- [IDTExtensibility2 のイベント プロシージャの使用](http://go.microsoft.com/fwlink/?LinkID=73471)
- [Office COM アドインを Visual Basic .NET でビルドします。](http://go.microsoft.com/fwlink/?LinkID=73469)
- [Office COM アドインを Visual C# .NET を使用してビルドします。](http://go.microsoft.com/fwlink/?LinkID=73472)
- [Office システム SE の Visual Studio 2005年のツールを使用して、InfoPath 2007 のアドインを作成します。](http://msdn.microsoft.com/en-us/library/bb968857%28office.12%29.aspx)

