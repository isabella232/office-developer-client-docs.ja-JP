---
title: InfoPath 2003 オブジェクト モデルを使用してデジタル署名を操作する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- デジタル署名 [infopath 2007],infopath 2003 互換のフォーム テンプレート,InfoPath 2003 互換のフォーム テンプレート,デジタル署名
localization_priority: Normal
ms.assetid: d6318238-fd45-4854-a3c9-c27c5685bd6b
description: InfoPath 2003 互換オブジェクト モデルは、デジタル署名をプログラムで操作する機能を提供します。
ms.openlocfilehash: 86e2c85c7515c896612df09b6186462480ceff61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299910"
---
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用してデジタル署名を操作する

InfoPath 2003 互換のオブジェクト モデルには、プログラムによってデジタル署名を操作する機能が用意されています。
  
## <a name="digital-signature-features"></a>デジタル署名の機能

InfoPath で使用できるデジタル署名機能では、以下の操作を行うことができます。 
  
- フォーム全体に署名する、またはフォーム内の署名可能な特定のデータ セットに個別に署名する。
    
- 署名対象にできる各データ セットについて、単一の署名または複数の署名が可能かどうかを指定し、その署名間の関係を指定する。たとえば、それらの署名を同等の連署にするのか、それとも新しい各署名を以前のすべての署名の副署にするのかを指定できます。
    
- ユーザーがフォームに署名したときにフォームに表示されるメッセージを指定する。
    
- 文書に署名を挿入し、それを確認する。 
    
- セキュリティ向上のために各署名に追加された検証可能な非否認情報を確認する。この追加情報には、各署名者に表示されたフォームのビューが含まれています。この追加情報は署名の一部になっていて、署名を無効にすることなく削除することはできません。このデータは、フォーム内の署名をクリックして [ **デジタル署名の確認**] ダイアログ ボックスを表示することにより、いつでも再表示できます。 
    
- デジタル署名の操作にオブジェクト モデルを活用する。デジタル署名のオブジェクト モデルを通じて、署名ブロックにカスタム情報を完全に信頼できる形で追加できます。 
    
## <a name="overview-of-the-digital-signatures-object-model"></a>デジタル署名のオブジェクト モデルの概要

### <a name="events"></a>イベント

デジタル署名のオブジェクト モデルには、次のイベントがあります。
  
|**[名前]**|**[説明]**|
|:-----|:-----|
|[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |署名するための一連の署名データが選択されたときに発生します。  <br/> このイベントを使用すると、デジタル署名に格納されているデータを操作することができます。たとえば、信頼されるタイムスタンプ サーバーからデータを追加したり、トランザクションのサーバー側副署名を追加したりできます。また、このイベントを使用すると、現在のユーザーが特定のグループのメンバーでない場合に署名を拒否することもできます。  <br/> |
   
**OnSign** イベントは、 [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) オブジェクトへの参照を返します。このオブジェクトには、次のプロパティが含まれています。 
  
|**[名前]**|**[説明]**|
|:-----|:-----|
|[ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |**OnSign** イベントから返された状態を示す **Boolean** 値を取得または設定します。  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |**OnSign** イベントを発生させた署名済みデータ ブロックを取得します。  <br/> |
|[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |**OnSign** イベントに関連付けられている **XDocument** オブジェクトへの参照を取得します。  <br/> |
   
### <a name="collections-and-objects"></a>コレクションおよびオブジェクト

デジタル署名のオブジェクト モデルには、次のコレクションがあります。
  
|**[名前]**|**[説明]**|
|:-----|:-----|
|[SignedDataBlocksCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |フォーム定義ファイル (.xsf) で定義されているフォーム テンプレート内の [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) オブジェクトのコレクション。  <br/> **SignedDataBlocksCollection** コレクションには、フォームに関連付けられている **SignedDataBlockObjects** オブジェクトにアクセスするためのプロパティがあります。 **SignedDataBlocks** コレクションへのアクセスには、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) オブジェクトの [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) プロパティを使用します。  <br/> |
|[SignaturesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |フォーム内の各 [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) に対する **SignatureObject** のコレクションが格納されています。  <br/> **SignaturesCollection** コレクションには、フォームに関連付けられている **SignatureObject** オブジェクトへのアクセスや、署名の作成に使用できるプロパティとメソッドが実装されています。このコレクションには、 **SignedDataBlockObject** オブジェクトを通じてアクセスできます。  <br/> [SignaturesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) コレクションの **Create** メソッドを使用する際には、 [SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) オブジェクトに対して **Sign** メソッドを呼び出すまでは署名が書き込まれないことを覚えておいてください。これらのメソッドは、完全に信頼されたフォーム テンプレートの **OnSign** イベント ハンドラーからしか呼び出せません。  <br/> |
   
デジタル署名のオブジェクト モデルには、次のオブジェクトがあります。
  
|**[名前]**|**[説明]**|
|:-----|:-----|
|[SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |フォーム内の署名可能な一連のデータを表します。 **SignedDataBlock** オブジェクトには、署名可能なデータ セットをプログラムで操作するために使用できる多数のプロパティと 1 つのメソッドがあります。  <br/> |
|[SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |フォームまたはフォーム内の署名可能な一連のデータに追加されたデジタル署名を表します。 **SignatureObject** コレクションには、デジタル署名に関する情報の取得に使用できる各プロパティ、および XML デジタル署名ブロックの書き込みとその暗号化ハッシュ値の計算のための [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) メソッドが実装されています。  <br/> |
|[CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |署名の作成に使用された X.509 デジタル証明書を表します。  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>プログラムでデジタル署名を操作する

InfoPath 2003 互換オブジェクト モデルには、デジタル署名をプログラムによって操作するための各種メンバーがあります。特に、完全に信頼されたフォームでは、次のようなタイムラインに従って、署名ブロックをコミットする前に署名ブロックにカスタム情報を追加することができます。
  
1. ユーザーがフォームにデジタル署名を追加する操作を開始します。
    
2. [ **デジタル署名ウィザード**] の最初のパネルが表示されます。 
    
3. **SignedDataBlockObject** オブジェクトによって表された選択中のデータの **OnSign** イベントが発生し、 **SignedDataBlockObject** の **Sign** メソッドおよび **SignaturesCollection** コレクションの **Create** メソッドが実行されます。 
    
4. 任意のオプション カスタム操作が実行されます。
    
5. **SignatureObject** の **Sign** メソッドが実行されます。 
    
6. 署名に使用する証明書を選択するためのウィザードの 2 つ目のパネル、およびコメントを入力するための 3 つ目のパネルが表示されます。
    
7. 非否認情報が表示されます (この情報は、後から [ **デジタル署名の確認**] ダイアログ ボックスでも確認できます)。 
    
8. [ **署名**] ボタンがクリックされると、そのフォーム用の署名のコレクションに署名が追加されます。 
    
次の例は、[ **署名**] ダイアログ ボックスを開いて、信頼できるタイムスタンプ サービスから取得したタイムスタンプ値で副署の署名を行います。 
  
```cs
[InfoPathEventHandler(EventType=InfoPathEventType.OnSign)]
public void OnSign(SignEvent e)
{
    Signature signature = e.SignedDataBlock.Signatures.Create();
    // Invoke the Sign dialog box to sign the data block.
    signature.Sign();
    // Countersign the signature with a trusted timestamp
    // Get the XML node storing the signature block
    IXMLDOMNode oNodeSig = signature.SignatureBlockXmlNode;
    IXMLDOMNode oNodeSigValue = oNodeSig.selectSingleNode(".//*[local-name(.)='signatureValue']");
    // Get timestamp from a trusted timestamp service (fictitious).
    MyTrustedTimeStampService s = new MyTrustedTimeStampService();
    string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.text);
    
    //Add the value returned from the timestamp service to the 
    //unsigned part of the signature block
    IXMLDOMNode oNodeObj = oNodeSig.selectSingleNode(".//*[local-name(.)='Object']");
    IXMLDOMNode oNode = oNodeObj.cloneNode(false);
    oNode.text = strVerifiedTimeStamp;
    oNodeObj.parentNode.appendChild(oNode);
    e.ReturnStatus = true;
}
```


