---
title: InfoPath にカスタム機能を追加する COM アドインを作成する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007、com アドインの作成、infopath 2007、カスタム機能の追加、com アドイン [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath は、ユーザーのフォーム編集を拡張する COM アドインをサポートしています。 最初に com アドインのサポートが InfoPath で追加されましたが、microsoft office Word や microsoft office Excel などの他の office アプリケーションでは、office 2000 以降の com アドインがサポートされています。
ms.openlocfilehash: f8dd16b161c4ea862cf3b15e56e26a2547c1fc4c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303788"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>InfoPath にカスタム機能を追加する COM アドインを作成する

Microsoft InfoPath は、ユーザーのフォーム編集を拡張する COM アドインをサポートしています。 最初に com アドインのサポートが InfoPath で追加されましたが、microsoft office Word や microsoft office Excel などの他の office アプリケーションでは、office 2000 以降の com アドインがサポートされています。
  
InfoPath での COM アドイン サポートはフォーム編集環境用に使用できます。 COM アドインを使用してもフォーム デザイン環境は拡張できません。
  
## <a name="the-idtextensibility2-interface"></a>IDTExtensibility2 インターフェイス

InfoPath 編集環境は、 **IDTExtensibility2**インターフェイスのサポートを提供します。これは、COM アドインの開発者によって実装されている必要があります。 **IDTExtensibility2**は、イベントとして機能する5つのメソッドを提供するデュアルインターフェイスオブジェクトです。編集環境内。 これらのメソッドにより、次の表に記載されている環境のスタートアップおよびシャットダウン条件に COM アドインが対応できます。 
  
|**インターフェイス**|**説明**|
|:-----|:-----|
|**onaddinsupdate (ByVal custom () As Variant)** <br/> |環境内でのアドインの読み込み時、またはアンロード時に発生します。  <br/> |
|**OnBeginShutdown ((Variant としての ByVal カスタム ())** <br/> |環境のシャット ダウン中に発生します。  <br/> |
|**OnConnection (byval Application as object, byval connectmode as ext_ConnectMode, byval addininst as object, byval custom () as Variant)** <br/> |アドインが環境に読み込まれると発生します。  <br/> |
|**OnDisconnection (byval removemode as ext_DisconnectMode, byval custom () as Variant)** <br/> |アドインが環境からアンロードされると発生します。  <br/> |
|**OnStartupComplete ((Variant としての ByVal カスタム ())** <br/> |環境の起動が完了すると発生します。  <br/> |
   
## <a name="registering-com-add-ins"></a>COM アドインの登録

InfoPath を含め、すべての Office アプリケーションはレジストリを使用して、COM アドイン コレクション内のアドインの一覧表示、接続状態の格納、ブートやデマンド読み込み情報の格納を行います。InfoPath COM アドインの場合、次のキーの下に、各アドインの名前が表示されます。
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
クライアント コンピューターのすべてのユーザーが使用できる COM アドインがインストールされている場合は、HKLM レジストリ ハイブにレジストリ キーがあります。
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
レジストリ キー名はアドインの **ProgIdAttribute** に対応し、次の値が含まれます。 
  
|**名前**|**Type**|**説明**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**String** <br/> |**[COM アドイン]** ダイアログ ボックスに表示され、**[セキュリティ センター]** の **[アドイン]** ページに 一覧表示される名前。  <br/> |
|**説明** <br/> |**String** <br/> |**[セキュリティ センター]** でアドインが選択されている場合に表示される文字列。  <br/> |
|**LoadBehavior** <br/> |**DWORD** <br/> |COM アドインの読み込み方法を指定します。 値は 0、1、2、8、および 16 を組み合わせたものです。 詳細については、次の表を参照してください。  <br/> |
   
**LoadBehavior** の **DWORD** 値には、編集環境での COM アドインの読み込み方法を示す値が含まれている必要があります。 次の表の値、または表中の値の組み合わせを指定できます。 たとえば、Visual Studio 2005 で作成される COM アドインには、アプリケーションの起動時に読み込まれた "3" の **LoadBehavior** が含まれ、接続されます。 
  
|**値**|**説明**|
|:-----|:-----|
|.0  <br/> |切断済み。アドインを **[COM アドイン]** のダイアログ ボックスに非アクティブとして表示します。<br/> |
|1-d  <br/> |接続済み。アドインを **[COM アドイン]** のダイアログ ボックスに アクティブとして表示します。<br/> |
|pbm-2  <br/> |起動時に読み込む。アドインは、ホスト アプリケーションの起動時に読み込まれ、接続されます。  <br/> |
|~  <br/> |必要時に読み込む。アドインは、ユーザーがアドインの機能を使用するボタンをクリックした時など、ホスト アプリケーションが要求した場合に読み込まれ、接続されます。  <br/> |
|16  <br/> |初回に接続する。アドインを登録した後にユーザーがホスト アプリケーションを実行した時に、アドインは初めて読み込まれます。  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Visual Studio 2005 または Visual Studio 2008 を利用したマネージ COM アドインの作成

Microsoft Visual Studio 2005 または Visual Studio 2008 を使用してマネージ COM アドインを作成するには、次の手順で共有アドイン プロジェクトを作成します。 
  
1. Visual Studio を起動します。
    
2. **[ファイル]** メニューの **[新しいプロジェクト]** をクリックします。
    
3. **[新しいプロジェクト]** ダイアログ ボックスの **[プロジェクトの種類]** ウィンドウで、**[その他のプロジェクトの種類]** フォルダーをクリックし、次に **[拡張]** をクリックします。
    
4. **[テンプレート]** ウィンドウで、**[共有アドイン]** をクリックします。
    
5. **[名前]** ボックスにプロジェクト名を入力します。 
    
6. **[場所]** ボックスにフォルダーのパスを入力するか、**[参照]** をクリックしてフォルダーのパスを選択し、**[OK]** をクリックします。**共有アドイン ウィザード**が表示されます。 
    
7. **共有アドイン ウィザード**で **[次へ]** をクリックします。 **[プログラミング言語の選択]** ページが表示されます。 
    
8. **[Visual Basic を使用してアドインを作成]** をクリックし、**[次へ]** をクリックします。 **[アプリケーション ホストの選択]** ページが表示されます。 
    
9. **Microsoft InfoPath** 以外の各アプリケーションの横にあるボックスのチェックを外して、**[次へ]** をクリックする。 **[名前と説明の入力]** ページが表示されます。 
    
10. **[アドインの名前]** ボックスに、COM アドインの名前を入力します。 
    
11. **[アドインの説明]** ボックスには、COM アドインの説明を入力し、**[次へ]** をクリックします。**[アドイン オプションの選択]** ページが表示されます。 
    
12. **[ホスト アプリケーションが読み込む時にマイ アドインを読み込む]** ボックスと **[マイ アドインをインストールするユーザーだけでなく、インストール先のコンピューターの全ユーザーが利用する]** ボックスをクリックします。 
    
13. **[次ヘ]** をクリックして **[概要]** ページを確認し、**[完了]** をクリックします。
    
Visual Studio によるプロジェクトの作成後に、2 つのプロジェクトが [ ソリューション エクスプローラー ] ウィンドウに表示されます。最初のプロジェクトは、COM アドイン用のプロジェクトです。2 番目のプロジェクトは、COM アドインを展開するためのセットアップ プロジェクトです。**共有アドイン ウィザード**は **Microsoft Office 14.0 オブジェクト ライブラリ**への参照を挿入するだけであるため、次の手順で InfoPath オブジェクト ライブラリへの参照を挿入する必要があります。
  
1. **[マイ プロジェクト]** をダブルクリックして、アドイン プロジェクトのプロパティを表示します。**[参照]** タブをクリックして、プロジェクトに自動的に追加された参照を表示します。 
    
2. **[追加]** ボタンをクリックして、**[参照の追加]** ダイアログ ボックスを表示します。 
    
3. **[COM]** タブの **[Microsoft.InfoPath 2.0 タイプ ライブラリ]** をダブルクリックし、**[OK]** をクリックします。
    
4. **[Microsoft InfoPath 3.0 タイプ ライブラリ]** への参照を追加すると、削除する必要のある 3 つのアセンブリ (**ADODB**、**MSHTML**、**MSXML2**) への参照も追加されます。 **References** の **Solution Explorer** で、これらの参照を右クリックし、次に **[削除]** をクリックします。
    
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
  
- [Office XP での管理された COM アドインの展開](https://go.microsoft.com/fwlink/?LinkID=73473)
  
- [com アドイン Shim ソリューションを使用して Office XP でマネージ COM アドインを展開する](https://go.microsoft.com/fwlink/?LinkID=73474)
  
- [COM Shim ウィザードを使用して Office 拡張機能を分離する](https://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> COM アドインを分離していない場合、メモリ リークが発生し、アプリケーションが不安定になる可能性があります。 
  
> [!NOTE]
> .NET Framework または設定プロジェクトが要求するその他の必要なアセンブリがターゲット コンピューターにインストールされていないと、.msi ファイルが正しくインストールされない可能性があります。また、.msi ファイルを配布するだけで .msi ファイルをインストールすることはできません。Visual Studio によって生成された元の .msi ファイルと同じフォルダー内の他のサポート ファイルも配布する必要があります。 
  
## <a name="coding-in-the-com-add-in"></a>COM アドインでのコーディング

InfoPath のフォーム編集環境で発生したアプリケーション イベントは、COM アドインでキャプチャできます。 COM アドインは、次のような[applicationevents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx)オブジェクトのイベントを使用して、ユーザー操作に応答できます。 
  
|**イベント**|**説明**|
|:-----|:-----|
|[newxdocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx)Event  <br/> |新しいフォームが作成されるときに発生します。  <br/> |
|[Quit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx)Event  <br/> |ユーザーが InfoPath を終了するときに発生します。  <br/> |
|[windowactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx)Event  <br/> |任意の文書ウィンドウがアクティブになるときに発生します。  <br/> |
|[windowdeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx)Event  <br/> |任意の文書ウィンドウが非アクティブになったときに発生します。  <br/> |
|[WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx)Event  <br/> |ドキュメント ウィンドウのサイズが変更されるとき、または移動されるときに発生します。  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx)Event  <br/> |開いている文書が閉じる直前に発生します。  <br/> |
|[xdocumentbeforeprint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx)Event  <br/> |開かれているドキュメントが印刷される直前に発生します。  <br/> |
|[xdocumentbeforesave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx)Event  <br/> |開かれているドキュメントが保存される直前に発生します。  <br/> |
|[xdocumentchange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx)Event  <br/> |新しいフォームが作成されるとき、既存のフォームが開かれるとき、または別のフォームがアクティブになるときに発生します。  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx)Event  <br/> |文書が開いたときに発生します。  <br/> |
   
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

最初の行は、アドインが受け取った汎用アプリケーション**オブジェクト**を[application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx)オブジェクトにキャストします。 2番目の行は、 **InfoPathApplication**変数で表される**application3**オブジェクトの[events](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx)プロパティを[applicationevents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx)オブジェクトにキャストします。 
  
イベント ハンドラーを作成するには、Visual Studio のウィンドウの上部にある **[クラス名]** ドロップダウン ボックスから **InfoPathApplicationEvents** を選択し、次に Visual Studio ウィンドウの上部にある **[メソッド名]** ドロップダウン ボックスから処理したいイベントを選択します。 たとえば、フォームを保存するタイミングをコントロールするには、**XDocumentBeforeSave** イベントを処理します。 **[メソッド名]** ドロップダウンから **XDocumentBeforeSave** を選択すると、次の手順を自動的に挿入します。 
  
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

- [Microsoft Office 2000 COM アドインを作成する](https://go.microsoft.com/fwlink/?LinkID=73468) 
- [Visual Studio .net を使用して Office マネージ COM アドインを作成する](https://go.microsoft.com/fwlink/?LinkID=73470)
- [IDTExtensibility2 イベントプロシージャを操作する](https://go.microsoft.com/fwlink/?LinkID=73471)
- [Visual Basic .net を使用して Office COM アドインをビルドする](https://go.microsoft.com/fwlink/?LinkID=73469)
- [Visual C# .net を使用して Office COM アドインをビルドする](https://support.microsoft.com/en-us/help/302901/how-to-build-an-office-com-add-in-by-using-visual-c-net)
- [Visual Studio 2005 Tools for Office System SE を使用して InfoPath 2007 アドインを作成する](https://msdn.microsoft.com/library/bb968857%28office.12%29.aspx)

