---
title: COM アドインを作成し、InfoPath にカスタム機能を追加する
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
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>COM アドインを作成し、InfoPath にカスタム機能を追加する

Microsoft InfoPath には、ユーザー エクスペリエンスの編集フォームを拡張するための COM アドインがサポートされています。 COM アドインが最初に追加した InfoPath では、他の Office アプリケーションなど、Microsoft Office Word と Microsoft Office Excel サポートされている COM アドインが Office 2000 以降をサポートします。
  
InfoPath での COM アドイン サポートはフォーム編集環境用に使用できます。COM アドインを使用してもフォーム デザイン環境は拡張できません。
  
## <a name="the-idtextensibility2-interface"></a>IDTExtensibility2 インターフェイス

InfoPath 編集環境は、**IDTExtensibility2** インターフェイスをサポートしますが、その実装は COM アドイン開発者が行う必要があります。**IDTExtensibility2** はデュアル インターフェイス オブジェクトで、編集環境内でイベントとして動作する 5 つのメソッドを提供します。これらのメソッドにより、次の表に記載されている環境のスタートアップおよびシャットダウン条件に COM アドインが対応できます。 
  
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
  
レジストリ キー名はアドインの **ProgIdAttribute** に対応し、次の値が含まれます。 
  
|**名前**|**型**|**説明**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**文字列型 (String)** <br/> |**[COM アドイン]** ダイアログ ボックスに表示され、**[セキュリティ センター]** の **[アドイン]** ページに 一覧表示される名前。  <br/> |
|**説明** <br/> |**String** <br/> |**[セキュリティ センター]** でアドインが選択されている場合に表示される文字列。  <br/> |
|**LoadBehavior** <br/> |**DWORD** <br/> |COM アドインの読み込み方法を指定します。値は 0、1、2、8、および 16 を組み合わせたものです。詳細については、次の表を参照してください。  <br/> |
   
**LoadBehavior** の **DWORD** 値には、編集環境での COM アドインの読み込み方法を示す値が含まれている必要があります。次の表の値、または表中の値の組み合わせを指定できます。たとえば、Visual Studio 2005 で作成される COM アドインには、アプリケーションの起動時に読み込まれた "3" の **LoadBehavior** が含まれ、接続されます。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |切断済み。アドインを **[COM アドイン]** のダイアログ ボックスに非アクティブとして表示します。<br/> |
|1  <br/> |接続済み。アドインを **[COM アドイン]** のダイアログ ボックスに アクティブとして表示します。<br/> |
|2  <br/> |起動時に読み込む。アドインは、ホスト アプリケーションの起動時に読み込まれ、接続されます。  <br/> |
|8  <br/> |必要時に読み込む。アドインは、ユーザーがアドインの機能を使用するボタンをクリックした時など、ホスト アプリケーションが要求した場合に読み込まれ、接続されます。  <br/> |
|16  <br/> |初回に接続する。アドインを登録した後にユーザーがホスト アプリケーションを実行した時に、アドインは初めて読み込まれます。  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Visual Studio 2005 または Visual Studio 2008 を利用したマネージ COM アドインの作成

Microsoft Visual Studio 2005 または Visual Studio 2008 を使用してマネージ COM アドインを作成するには、次の手順で共有アドイン プロジェクトを作成します。  
  
1. Visual Studio を起動します。
    
2. **[ファイル]** メニューの **[新しいプロジェクト]** をクリックします。
    
3. **[新しいプロジェクト]** ダイアログ ボックスの **[プロジェクトの種類]** ウィンドウで、**[その他のプロジェクトの種類]** フォルダーをクリックし、次に **[拡張]** をクリックします。
    
4. **[テンプレート]** ウィンドウで、**[共有アドイン]** をクリックします。
    
5. **[名前]** ボックスにプロジェクト名を入力します。 
    
6. **[場所]** ボックスにフォルダーのパスを入力するか、**[参照]** をクリックしてフォルダーのパスを選択し、**[OK]** をクリックします。**共有アドイン ウィザード**が表示されます。 
    
7. **共有アドイン ウィザード**で **[次へ]** をクリックします。**[プログラミング言語の選択]** ページが表示されます。 
    
8. **[Visual Basic を使用してアドインを作成]** をクリックし、**[次へ]** をクリックします。**[アプリケーション ホストの選択]** ページが表示されます。 
    
9. **Microsoft InfoPath** 以外の各アプリケーションの横にあるボックスのチェックを外して、**[次へ]** をクリックする。**[名前と説明の入力]** ページが表示されます。 
    
10. **[アドインの名前]** ボックスに、COM アドインの名前を入力します。 
    
11. **[アドインの説明]** ボックスには、COM アドインの説明を入力し、**[次へ]** をクリックします。**[アドイン オプションの選択]** ページが表示されます。 
    
12. **[ホスト アプリケーションが読み込む時にマイ アドインを読み込む]** ボックスと **[マイ アドインをインストールするユーザーだけでなく、インストール先のコンピューターの全ユーザーが利用する]** ボックスをクリックします。 
    
13. **[次ヘ]** をクリックして **[概要]** ページを確認し、**[完了]** をクリックします。
    
Visual Studio によるプロジェクトの作成後に、2 つのプロジェクトが [ ソリューション エクスプローラー ] ウィンドウに表示されます。最初のプロジェクトは、COM アドイン用のプロジェクトです。2 番目のプロジェクトは、COM アドインを展開するためのセットアップ プロジェクトです。**共有アドイン ウィザード**は **Microsoft Office 14.0 オブジェクト ライブラリ**への参照を挿入するだけであるため、次の手順で InfoPath オブジェクト ライブラリへの参照を挿入する必要があります。
  
1. **[マイ プロジェクト]** をダブルクリックして、アドイン プロジェクトのプロパティを表示します。**[参照]** タブをクリックして、プロジェクトに自動的に追加された参照を表示します。 
    
2. **[追加]** ボタンをクリックして、**[参照の追加]** ダイアログ ボックスを表示します。 
    
3. **[COM]** タブの **[Microsoft.InfoPath 2.0 タイプ ライブラリ]** をダブルクリックし、**[OK]** をクリックします。
    
4. **[Microsoft InfoPath 3.0 タイプ ライブラリ]** への参照を追加すると、削除する必要のある 3 つのアセンブリ (**ADODB**、**MSHTML**、**MSXML2**) への参照も追加されます。**References** の **Solution Explorer** で、これらの参照を右クリックし、次に **[削除]** をクリックします。
    
## <a name="viewing-the-registry-settings"></a>レジストリ設定の表示

COM アドインのインストール時に作成されるレジストリ設定を表示するには、以下の手順を実行します。
  
1. **[ソリューション エクスプローラー]** にある設定プロジェクトのルート ノードを右クリックし、**[表示]**、**[エディター]**、**[レジストリ]** を順番にクリックします。
    
2. 左側のウィンドウで、プラス記号をクリックして **[HKEY_LOCAL_MACHINE]**、**[ソフトウェア]**、**[Microsoft]**、**[InfoPath]**、**[アドイン]** を順番にクリックします。
    
3. 共有アドイン プロジェクトの **ProgID** に対応する名前をクリックします。
    
これらのプロパティのいずれかを変更するには、プロパティを右クリックし、**[プロパティ ウィンドウ]** をクリックして、**プロパティ ウィンドウ**の **[値]** ボックスを変更します。
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>共有アドインのコンパイルと配布

共有アドイン プロジェクトが開発されたコンピューターでテストするためにマネージ COM アドインをコンパイルするには、ソリューション エクスプローラーで共有アドイン プロジェクトのルート ノードを右クリックし、[ビルド] をクリックします。エラーが出ずにプロジェクトがビルドすると、InfoPath 編集環境を起動し、マネージ COM アドインの使用を開始できます。実行中の InfoPath のインスタンスがある場合は、プロジェクトをビルドする前に閉じてください。COM アドインが登録されていることを確認するために、[COM アドイン] ダイアログ ボックスを開く必要がある場合があります。[COM アドイン] ダイアログ ボックスは、次の手順で開きます。
  
1. InfoPath 編集環境を開く最も簡単な方法は、既存のフォーム テンプレートを開きます。すると、そのフォーム テンプレートに基づいて新しいフォームが作成されます。
    
2. **[ツール]** メニューの **[セキュリティ センター]** をクリックします。 
    
3. 左側の **[アドイン]** カテゴリをクリックします。 
    
4. **[セキュリティ センター]** ダイアログ ボックスの下部近くにある **[管理]** セクションで、リストから **[COM アドイン]** を選択し、**[移動]** ボタンをクリックします。 
    
5. **[COM アドイン]** ダイアログ ボックスに、最近ビルドしたアドインの名前が表示され、その横にチェック ボックスがあります。横にチェック ボックスがない場合は、エラーにより COM アドインの読み込みが失敗しています。この失敗についてはダイアログ ボックスの **[読み込み時の動作]** セクションの一覧に含められます。 
    
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
  
|**イベント**|**説明**|
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
   
COM アドインでこれらのイベントをキャプチャするには、**Connect** クラス内のクラス レベル変数を宣言する必要があります。 
  
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
  
イベント ハンドラーを作成するには、Visual Studio のウィンドウの上部にある **[クラス名]** ドロップダウン ボックスから **InfoPathApplicationEvents** を選択し、次に Visual Studio ウィンドウの上部にある **[メソッド名]** ドロップダウン ボックスから処理したいイベントを選択します。たとえば、フォームを保存するタイミングをコントロールするには、**XDocumentBeforeSave** イベントを処理します。**[メソッド名]** ドロップダウンから **XDocumentBeforeSave** を選択すると、次の手順を自動的に挿入します。 
  
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

**ApplicationEvents** オブジェクトのいずれのイベントも、同じメソッドを使用する COM アドインで処理することができます。 
  
## <a name="see-also"></a>関連項目

- [Microsoft Office 2000 COM アドインを作成します。](http://go.microsoft.com/fwlink/?LinkID=73468) 
- [マネージ COM アドインが Visual Studio .NET での Office を作成します。](http://go.microsoft.com/fwlink/?LinkID=73470)
- [IDTExtensibility2 のイベント プロシージャの使用](http://go.microsoft.com/fwlink/?LinkID=73471)
- [Office COM アドインを Visual Basic .NET でビルドします。](http://go.microsoft.com/fwlink/?LinkID=73469)
- [Office COM アドインを Visual C# .NET を使用してビルドします。](http://go.microsoft.com/fwlink/?LinkID=73472)
- [Office システム SE の Visual Studio 2005年のツールを使用して、InfoPath 2007 のアドインを作成します。](http://msdn.microsoft.com/en-us/library/bb968857%28office.12%29.aspx)

