---
title: 完全に信頼できるフォームを理解する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64d62990-6275-edef-c639-b6ba8d10c38c
description: InfoPath には、完全に信頼できるフォーム (セキュリティのより高いアクセス許可があり、ユーザーのコンピューターのシステム リソースおよびその他のコンポーネントにアクセスできるフォーム) を作成する機能があります。この記事では、完全に信頼できるフォームとは何か、このフォームを使用する理由、および標準のフォームを手動で変換および登録するか、または標準のフォームにデジタル署名して、完全に信頼できるフォームを作成する方法について説明します。
ms.openlocfilehash: b410d5bee0080aae5e0af9687999595655b42edf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799218"
---
# <a name="understanding-fully-trusted-forms"></a>完全に信頼できるフォームを理解する

InfoPath には、完全に信頼できるフォーム (セキュリティのより高いアクセス許可があり、ユーザーのコンピューターのシステム リソースおよびその他のコンポーネントにアクセスできるフォーム) を作成する機能があります。この記事では、完全に信頼できるフォームとは何か、このフォームを使用する理由、および標準のフォームを手動で変換および登録するか、または標準のフォームにデジタル署名して、完全に信頼できるフォームを作成する方法について説明します。

InfoPath フォーム テンプレートは、さまざまなレベルのセキュリティと共に展開できます。使用するレベルは、フォームで外部リソースにアクセスするために必要なレベルによって決まります。既定では、InfoPath フォーム テンプレートはシステム リソースへのアクセスを制限され、スクリプトを実行しても安全であるとマークされていないソフトウェア コンポーネントの使用は許可されません。ただし、この動作を無効にし、システム リソースや、スクリプトを実行しても安全であるとマークされていないソフトウェア コンポーネントを含むその他の外部リソースに、フォームがアクセスすることを許可できます。
  
フォームを使用するには、フォームの基になっているフォーム テンプレートに InfoPath がアクセスできる必要があります。 InfoPath でフォーム テンプレートを作成すると、フォーム テンプレートの場所の URL を含むエントリが、フォーム定義ファイル (.xsf) に作成されます。 URL ベース フォームと呼ばれます*サンド ボックス化されました*。 ユーザーがこのフォームに入力すると、フォームはローカル キャッシュに追加され、システム リソースへのアクセスを拒否されます。 この種類のフォームは、フォームが開かれたドメインからアクセス許可を継承します。 
  
ただし、フォームを変更し、システム リソースへのアクセスが許可される URN (Uniform Resource Name) ベースのフォームにすることができます。 この種のフォームは、*完全に信頼*すると見なされます。 
  
## <a name="why-use-a-fully-trusted-form"></a>完全に信頼できるフォームを使用する理由

完全に信頼できるフォームには、セキュリティで保護されたフォームよりも高いアクセス許可のセットが与えられます。たとえば、システム リソースにアクセスするために外部オブジェクトを使用するプログラミング コードを含むこと、スクリプトを実行しても安全であるとマークされていないソフトウェア コンポーネントまたは Microsoft ActiveX コントロールを使用すること、および .NET アセンブリで提供されるカスタム ビジネス ロジックを使用することができます。
  
さらに、InfoPath オブジェクト モデルの一部のメンバーはセキュリティ レベル 3 に設定されます。これは、それらのメンバーが完全に信頼できるフォームのみで使用できることを意味します。たとえば、Microsoft Office **CommandBars** オブジェクトにアクセスするには、InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) クラスの [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) プロパティを使用して、メンバーへの参照を設定します。このプロパティはセキュリティ レベル 3 に設定されるので、完全に信頼されていないフォームでは使用できません。 
  
> [!NOTE]
> [!メモ] 完全に信頼されていないフォームで、[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) クラスの [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) プロパティ、またはセキュリティ レベルが 3 のその他のオブジェクト モデル メンバーを使用すると、"アクセスは拒否されました" というエラーが発生します。 
  
## <a name="what-makes-a-form-fully-trusted"></a>フォームを完全に信頼する方法

完全に信頼できるフォームの作成と使用には、InfoPath ユーザー インターフェイスとフォーム ファイルの両方が関連する、次の操作が必要です。
  
- [ **セキュリティ センター**] ダイアログ ボックスの [ **信頼できる発行元**] カテゴリで、InfoPath が完全に信頼できるフォームの使用を許可するようにする。このオプションは、完全に信頼できるフォームをユーザーが開けるようにするために有効にする必要があります。 
    
- InfoPath **Application** オブジェクトの **RegisterSolution** メソッドを使用して、完全に信頼できるフォームをターゲット コンピューターに登録する。 
    
## <a name="creating-a-fully-trusted-form"></a>完全に信頼できるフォームを作成する

- フォームを手動で作成することができます。これには、フォーム ファイルの一部を直接変更する操作が必要になります。
    
- フォーム テンプレートにデジタル署名することができます。
    
### <a name="manually-creating-a-fully-trusted-form"></a>完全に信頼できるフォームを手動で作成する

#### <a name="to-manually-create-a-fully-trusted-form"></a>完全に信頼できるフォームを手動で作成するには

1. 完全に信頼できるようにするフォーム テンプレートのバックアップ コピーを作成します。
    
2. InfoPath でフォーム テンプレートを開きます。
    
3. フォームのソース ファイルをハード ディスク上のフォルダーに保存します。そのためには、[ **ファイル**] タブ、[ **発行**]、[ **ソース ファイルのエクスポート**] の順にクリックします。
    
4. フォームのソース ファイルを保存するフォルダーを指定し、[ **OK**] をクリックします。次に、InfoPath デザイナーを終了します。
    
5. フォーム ファイルを抽出したフォルダーで、既定では  `manifest.xsf` という名前のフォーム定義ファイル (.xsf) を、Microsoft メモ帳などのテキスト エディターで開きます。 
    
6. .xsf ファイルの **xDocumentClass** 要素に、次の属性を追加します。 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > [!メモ] URN に使用する値は、その値が一意である限り、任意の種類の文字列値とすることができます。 後の少なくとも 2 つの値が存在する必要があります、`urn:`プレフィックス、およびこれらの値はコロンで区切る必要があります。 さらに、URN は 255 文字を超えることはできません。 
  
7. .xsf ファイルを保存して閉じ、既定では  `Template.xml` という名前の XML テンプレート ファイル (.xml) を、メモ帳などのテキスト エディターで開きます。 
    
8. **href** 属性を  `mso-infoPathSolution` 処理命令から削除し, .xsf ファイルの手順 6. で使用したのと同じ **name** 属性に置き換えます。 
    
   > [!NOTE]
   > [!メモ] **name** 属性に使用される URN 値は, .xsf ファイルと XML テンプレート ファイルの両方で同じである必要があります。 
  
9. XML テンプレート ファイルを保存して閉じます。
    
10. makecab.exe などのツールを使用して、ファイルを .xsn CAB 形式に再パッケージ化します。
    
    > [!NOTE]
    > [!メモ] InfoPath フォーム デザイナーはフォーム ファイルの .xsn ファイルへの再パッケージ化をサポートしていますが、この処理を実行すると、フォームが URL ベースのフォームに戻ります。このため、変更がフォーム ファイルに上書きされないようにするには、ファイルを手動で再パッケージ化する必要があります。 
  
11. InfoPath **Application** オブジェクトの **RegisterSolution** メソッドを使用してカスタム インストール プログラムを作成して、完全に信頼できるフォームをインストールします。このための簡単な方法は、次のコード行を使用するスクリプト ファイルを、Microsoft JScript または VBScript 構文のどちらかで作成することです。 
    
    ```js
        objIPApp = new ActiveXObject("InfoPath.Application"); 
        objIPApp.RegisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
        objIPApp.Quit(); 
        objIPApp = null;
    ```
   
    ```vb
        Public Sub InstallForm()
            Dim objIPApp As Object
            ' Create a reference to the Application object.
            Set objIPApp = CreateObject("InfoPath.Application")
            ' Register the InfoPath form template.
            objIPApp.RegisterSolution ("C:\\My Forms\\MyFormTemplate.xsn")
            MsgBox "The InfoPath form template has been registered."
            Set objIPApp = Nothing
        End Sub
        
    ```

> [!NOTE] 
> [!メモ] この例では簡単なスクリプト ファイルを使用していますが、Microsoft Windows インストーラー (.msi) ファイルなどの、より堅牢なインストール メカニズムを使用することもできます。ただし、 **RegisterSolution** メソッドを使用して、完全に信頼できるフォームをターゲット コンピューターに正しくインストールしてください。Visual Basic または Visual Studio から、InfoPath **Application** オブジェクトの **RegisterSolution** メソッドにアクセスするには、Microsoft InfoPath 3.0 タイプ ライブラリへの参照を設定します。これは、C:\Program Files\Microsoft Office\Office14 フォルダーにインストールされる IPEDITOR.dll によって提供されます。 
  
完全に信頼できるフォームを削除する必要がある場合は、次の JScript および VBScript の例に示すように、 **Application** オブジェクトの **UnregisterSolution** メソッドを使用できます。 
    
```js
    objIPApp = new ActiveXObject("InfoPath.Application"); 
    objIPApp.UnregisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
    objIPApp.Quit(); 
    objIPApp = null;
```

```vb
    Public Sub UninstallForm()
        Dim objIPApp As Object
        ' Create a reference to the Application object.
        Set objIPApp = CreateObject("InfoPath.Application")
        ' Unregister the InfoPath form template.
        objIPApp.UnregisterSolution ("C:\My Forms\MyFormTemplate.xsn")
        MsgBox ("The InfoPath form template has been unregistered.")
        Set objIPApp = Nothing
    End Sub
    
```

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a>フォーム テンプレートにデジタル署名して完全に信頼できるフォームを作成する

フォーム テンプレートにデジタル署名を使用すると、電子メールで、または Microsoft SharePoint Foundation を実行しているサーバーなど、Web サーバー上に完全に信頼されたフォーム テンプレートを展開します。 フォームの完全な信頼を指定し、デジタル署名して発行することによりフォームを完全に信頼するには、次の 3 つの手順を使用します。
  
#### <a name="to-digitally-sign-a-form-template"></a>フォーム テンプレートにデジタル署名するには

1. フォームを InfoPath デザイナーで開き、[ **ファイル**] タブをクリックし、[ **情報**] タブの [ **フォームのオプション**] をクリックします。 
    
2. [ **フォームのオプション**] ダイアログ ボックスの [ **セキュリティと信頼**] カテゴリをクリックします。 
    
3. [ **自動的にセキュリティ レベルを設定する (推奨)**] チェック ボックスをオフにします。
    
4. [ **完全信頼 (コンピューターにあるファイルおよび設定にアクセスできる)**] をクリックします。
    
5. [ **フォーム テンプレートの署名**] の [ **このフォーム テンプレートに署名する**] チェック ボックスをオンにします。
    
6. [ **証明書の選択**] をクリックして、信頼されている証明書プロバイダーから以前にダウンロードおよびインストールされている証明書を選択します。 
    
7. [OK] を 2 回クリックして完全に終了します。
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a>フォーム テンプレートを SharePoint ドキュメント ライブラリに発行するには

1. [ **ファイル**] タブの [ **発行**] をクリックし、[ **SharePoint Server**] をクリックします。
    
2. [ **発行ウィザード**] の指示に従って、フォーム テンプレートを新しい SharePoint ドキュメント ライブラリまたは既存の SharePoint ドキュメント ライブラリに発行します。 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a>完全に信頼できるデジタル署名されたフォーム テンプレートに基づいてフォームを作成するには

1. SharePoint ドキュメント ライブラリで、[ **フォームの入力**] をクリックします。
    
   > [!NOTE]
   > [!メモ] [ **発行ウィザード**] を使用して SharePoint ドキュメント ライブラリにフォーム テンプレートを発行しても、テンプレートはフォーム ライブラリの項目として表示されません。このドキュメント ライブラリでフォームを作成すると、テンプレートは、新しいフォームのテンプレートとして既定で使用されます。 
  
2. InfoPath では、既定のフォーム テンプレートがデジタル署名されている場合、デジタル署名されたフォーム テンプレートに関するセキュリティ警告が表示されます。[ **この発行元のファイルを常に信頼し、自動的にファイルを開く**] をクリックし、[ **開く**] をクリックします。
    
## <a name="using-a-fully-trusted-form"></a>完全に信頼できるフォームを使用する

完全に信頼できるフォームの使用は、標準のフォームの使用に非常に似ています。唯一の重要な違いは、制限されたリソースにフォームがアクセスすることができ、警告は表示されないことです。
  
> [!NOTE]
> [!メモ] InfoPath で完全に信頼できるフォームを有効にするには、ユーザーは [ **セキュリティ センター**] ダイアログ ボックスの [ **信頼できる発行元**] カテゴリで [ **完全に信頼できるフォームをこのコンピューターで実行できるようにする**] チェック ボックスがオンになっていることを確認する必要があります。[ **セキュリティ センター**] ダイアログ ボックスを開くには、[ **ファイル**] タブ、([ **InfoPath**] タブの下にある) [ **オプション**]、[ **セキュリティ センター**]、[ **セキュリティ センターの設定**] の順にクリックします。 
  
完全に信頼できるフォームは InfoPath の [ **フォームの入力**] ダイアログ ボックスから開くことができます。 
  
[ **フォームの入力**] ダイアログ ボックスを開くには、[ **フォームの入力**] 作業ウィンドウの [ **その他のフォーム**] をクリックするか、または [ **ファイル**] メニューの [ **フォームの入力**] をクリックします。 
  
### <a name="making-changes-to-a-fully-trusted-form"></a>完全に信頼できるフォームに変更を加える

.xsn ファイルに変更を加えるだけの場合は、変更後に、ユーザーが既存の .xsn ファイルを新しいファイルに置き換えるようにします。ユーザーがカスタム インストール プログラムを使用してファイルを再インストールする必要はありません。
  
ただし, .xsn ファイルに含まれているフォーム ファイルに変更を加える場合は、前に説明したように、ファイルを再パッケージ化し、完全に信頼できるフォームをユーザーが再インストールする必要があります。
  
> [!NOTE]
> [!メモ] 最善の方法は、InfoPath デザイナーからフォーム テンプレートを .xsn 形式に戻して保存し、この記事の手順に従って、完全に信頼できるフォームを作成することです。 
  
## <a name="conclusion"></a>まとめ

ビジネスの要件やユーザーのニーズによっては、標準の InfoPath フォームよりも高いアクセス許可のセットが与えられたフォームの作成が必要になることもあります。InfoPath には、フォームを変更することで、システム リソース、およびスクリプトを実行しても安全であるとマークされていないその他の外部リソースにアクセスできるようにする機能があります。この操作は、フォーム テンプレートに含まれるフォーム ファイルを変更し、インストール スクリプトを実行するか、またはフォーム テンプレートにデジタル署名することにより、手動で行うことができます。
  

