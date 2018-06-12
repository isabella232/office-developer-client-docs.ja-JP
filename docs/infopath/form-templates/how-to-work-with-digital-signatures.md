---
title: デジタル署名を使用します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- digital signatures [infopath 2007],InfoPath 2007, digital signatures
localization_priority: Normal
ms.assetid: fd13fb71-aecf-47bb-8a6b-db70bd90ceeb
description: Microsoft.Office.InfoPath 名前空間のオブジェクト モデルには、デジタル署名をプログラムによって操作するための機能が用意されています。
ms.openlocfilehash: 1277998edf4feb94da40d82372fd4d96fedf2d54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799169"
---
# <a name="work-with-digital-signatures"></a>デジタル署名を使用します。

[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間のオブジェクト モデルには、デジタル署名をプログラムによって操作するための機能が用意されています。 
  
## <a name="digital-signature-features"></a>デジタル署名の機能

InfoPath のデジタル署名機能を使用すると、以下の操作を行うことができます。 
  
- フォーム全体に署名する、またはフォーム内の署名可能な特定のデータ セットに個別に署名する。
    
- 署名対象にできる各データ セットについて、単一の署名または複数の署名が可能かどうかを指定し、その署名間の関係を指定する。たとえば、それらの署名を同等の連署にするのか、それとも新しい各署名を以前のすべての署名の副署にするのかを指定できます。
    
- ユーザーがフォームに署名したときにフォームに表示されるメッセージを指定する。
    
- 文書に署名を挿入し、それを確認する。 
    
- セキュリティ向上のために各署名に追加された検証可能な非否認情報を確認する。この追加情報には、各署名者に表示されたフォームのビューが含まれています。この追加情報は署名の一部になっていて、署名を無効にすることなく削除することはできません。このデータは、フォーム内の署名をクリックして [ **デジタル署名の確認**] ダイアログ ボックスを表示することにより、いつでも再表示できます。 
    
- デジタル署名の操作にオブジェクト モデルを活用する。デジタル署名のオブジェクト モデルを通じて、署名ブロックにカスタム情報を完全に信頼できる形で追加できます。 
    
## <a name="overview-of-the-digital-signatures-object-model"></a>デジタル署名のオブジェクト モデルの概要

### <a name="the-sign-event"></a>Sign イベント

デジタル署名のオブジェクト モデルには、次のイベントがあります。
  
|**名前**|**説明**|
|:-----|:-----|
|[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |署名するための一連のデータが選択されたときに発生します。  <br/> このイベントを使用すると、デジタル署名に格納されているデータを操作することができます。たとえば、信頼されるタイムスタンプ サーバーからデータを追加したり、トランザクションのサーバー側副署名を追加したりできます。また、このイベントを使用すると、現在のユーザーが特定のグループのメンバーでない場合に署名を拒否することもできます。  <br/> |
   
### <a name="the-signeventargs-object"></a>SignEventArgs オブジェクト

[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) イベントのイベント ハンドラーは、 [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) イベント オブジェクトで動作します。このイベント オブジェクトには、次のプロパティがあります。 
  
|**名前**|**説明**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) イベントを発生させたデータのセットを取得します。  <br/> |
|[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |[ **デジタル署名**] ダイアログ ボックスを表示するかどうかを取得または設定します。  <br/> |
   
> [!NOTE]
> [!メモ] InfoPath 2003 に付属している [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) マネージ コード オブジェクト モデルで、 [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) イベントの [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) イベント オブジェクトには、イベントに関連付けられているフォームの **XDocument** オブジェクトにアクセスするための **XDocument** プロパティがあります。このプロパティは、InfoPath Forms Services または InfoPath で [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) オブジェクト モデルを使用して作成されたフォーム テンプレートでは必要ありません。 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) クラスのオブジェクト モデル メンバーは、フォーム コード内で **this** (C# の場合) キーワードまたは **Me** (Visual Basic の場合) キーワードを使用してアクセスできるからです。たとえば、 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) クラスの [Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティにアクセスして、フォームが署名されているかどうかを判別するには、  `this.Signed` または  `Me.Signed.` を入力できます。
  
### <a name="collections-and-objects"></a>コレクションおよびオブジェクト

デジタル署名のオブジェクト モデルには、次のコレクションがあります。
  
|**名前**|**説明**|
|:-----|:-----|
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |InfoPath のデザイン モードでデザイン時に定義されたフォーム テンプレート内の [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) オブジェクトのコレクション。  <br/> [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) コレクションは、フォームに関連付けられている [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) オブジェクトへのアクセスに使用できるプロパティを実装しています。フォームに関連付けられている [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) オブジェクトは、 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) クラスの [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティを使用してアクセスできます。  <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |フォーム内の各 [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) オブジェクトの [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) オブジェクトのコレクションが格納されています。  <br/> [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) クラスには、フォームに関連付けられている [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) オブジェクトへのアクセスや、署名の作成に使用できるプロパティとメソッドが実装されています。 [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) に関連付けられている [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) オブジェクトは、 [Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) プロパティを使用してアクセスできます。  <br/> [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) クラスの [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) メソッドを使用するときは、 [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) オブジェクトに対して [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) メソッドを呼び出すまでは署名が書き込まれないことを覚えておいてください。これらのメソッドは、完全に信頼されたフォーム テンプレートの **Sign** イベント ハンドラーからしか呼び出せません。  <br/> |
   
デジタル署名のオブジェクト モデルには、次のオブジェクトがあります。
  
|**名前**|**説明**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |フォーム内の署名可能な一連のデータを表します。[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) オブジェクトには、署名可能なデータ セットをプログラムで操作するために使用できる多数のプロパティと 1 つのメソッドがあります。<br/> |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |フォームまたはフォーム内の署名可能な一連のデータに追加されたデジタル署名を表します。[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) オブジェクトには、デジタル署名に関する情報の取得に使用できる各プロパティ、および XML デジタル署名ブロックの書き込みとその暗号化ハッシュ値の計算のための [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) メソッドが実装されています。<br/> |
|[Certificate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |署名の作成に使用された X.509 デジタル証明書を表します。  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>プログラムでデジタル署名を操作する

[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間のオブジェクト モデルには、デジタル署名をプログラムによって操作するためのメンバーが用意されています。特に、完全に信頼されたフォームでは、次のようなタイムラインに従って、署名ブロックをコミットする前に署名ブロックにカスタム情報を追加することができます。 
  
1. ユーザーがフォームにデジタル署名を追加する操作を開始します。
    
2. [ **デジタル署名**] ダイアログ ボックスが表示され、ユーザーは [ **追加**] をクリックし、署名するデータを選択します。
    
3. [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) オブジェクトによって表されている選択されたデータの [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) イベントが発生し、 [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) オブジェクトの [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) メソッドおよび [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) コレクションの [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) メソッドが実行されます。 
    
4. 任意のオプション カスタム操作が実行されます。
    
5. [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) オブジェクトの [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) メソッドが実行されます。 
    
6. 名前の入力 (または署名画像の選択)、署名に使用する証明書の選択、およびコメントの入力を行うための [ **署名**] ダイアログ ボックスが表示されます。 
    
7. [ **署名**] ボタンがクリックされると、そのフォーム用の署名のコレクションに署名が追加され、非否認情報がキャプチャされて署名と共に保存されます (非否認情報は、後で [ **デジタル署名**] ダイアログ ボックスの [ **署名済みフォームの表示**] をクリックし、[ **収集された追加署名情報の表示**] をクリックすることで確認できます)。
    
次の例では、ユーザーが、選択されたデータの署名と、信頼できるタイムスタンプ サービスから取得したタイムスタンプ値で副署の署名を行うとき、[Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) メソッドを呼び出します。 
  
```cs
public void FormEvents_Sign(object sender, SignEventArgs e)
{
   // Add a new Signature object to the SignedDataBlockCollection.
   Signature thisSignature = 
      e.SignedDataBlock.Signatures.CreateSignature();
   // Write the XML digital signature block and compute hash
   // for signed data.
   thisSignature.Sign();
   // Countersign the signature with a trusted timestamp.
   // Get the XML node storing the signature block.
   XPathNavigator oNodeSig = thisSignature.SignatureBlockXmlNode;
   XPathNavigator oNodeSigValue = 
      oNodeSig.SelectSingleNode(
      ".//*[local-name(.)='signatureValue']");
   // Get timestamp from a trusted timestamp service (fictitious).
   MyTrustedTimeStampService s = new MyTrustedTimeStampService();
   string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.Value);
   // Add the value returned from the timestamp service to the 
   // unsigned part of the signature block.
   XPathNavigator oNodeObj = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']");
   XPathNavigator oNode = oNodeObj.Clone();
   oNode.SetValue(strVerifiedTimeStamp);
   oNodeObj.MoveToParent();
   oNodeObj.AppendChild(oNode);
   e.SignatureWizard = false;
}
```

```vb
Public Sub FormEvents_Sign(ByVal sender As Object, _
   ByVal e As SignEventArgs)
   ' Add a new Signature object to the SignedDataBlockCollection.
   Dim thisSignature As Signature = 
      e.SignedDataBlock.Signatures.CreateSignature
   ' Write the XML digital signature block and compute hash
   ' for signed data.
   thisSignature.Sign()
   ' Countersign the signature with a trusted timestamp.
   ' Get the XML node storing the signature block
   Dim oNodeSig As XPathNavigator  = _
      thisSignature.SignatureBlockXmlNode
   Dim oNodeSigValue As XPathNavigator  = _
      oNodeSig.SelectSingleNode(_
      ".//*[local-name(.)='signatureValue']")
   ' Get timestamp from a trusted timestamp service (fictitious).
   Dim s As MyTrustedTimeStampService = New MyTrustedTimeStampService()
   Dim strVerifiedTimeStamp As String  = _
      s.AddTimeStamp(oNodeSigValue.Value)
   ' Add the value returned from the timestamp service to the 
   ' unsigned part of the signature block.
   Dim oNodeObj As XPathNavigator  = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']")
   Dim oNode As XPathNavigator  = oNodeObj.Clone()
   oNode.SetValue(strVerifiedTimeStamp)
   oNodeObj.MoveToParent()
   oNodeObj.AppendChild(oNode)
   e.SignatureWizard = False
```


