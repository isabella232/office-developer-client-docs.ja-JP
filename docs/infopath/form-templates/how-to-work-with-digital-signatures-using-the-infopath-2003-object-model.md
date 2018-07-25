---
title: InfoPath 2003 オブジェクト モデルを使用してデジタル署名を操作する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- デジタル署名 [infopath 2007],infopath 2003 互換のフォーム テンプレート,InfoPath 2003 互換のフォーム テンプレート,デジタル署名
localization_priority: Normal
ms.assetid: d6318238-fd45-4854-a3c9-c27c5685bd6b
description: InfoPath 2003 互換のオブジェクト モデルには、プログラムによってデジタル署名を操作する機能が用意されています。
ms.openlocfilehash: ae9934e36766b7e783d1404a12a49e9b0b08543a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799134"
---
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a><span data-ttu-id="2f6cf-104">InfoPath 2003 オブジェクト モデルを使用してデジタル署名を操作する</span><span class="sxs-lookup"><span data-stu-id="2f6cf-104">How to: Work with Digital Signatures Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="2f6cf-105">InfoPath 2003 互換のオブジェクト モデルには、プログラムによってデジタル署名を操作する機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-105">The InfoPath 2003-compatible object model provides features for working with digital signatures programmatically.</span></span>
  
## <a name="digital-signature-features"></a><span data-ttu-id="2f6cf-106">デジタル署名の機能</span><span class="sxs-lookup"><span data-stu-id="2f6cf-106">Digital Signature Features</span></span>

<span data-ttu-id="2f6cf-107">InfoPath で使用できるデジタル署名機能では、以下の操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-107">The digital signatures features available in InfoPath enable you to:</span></span> 
  
- <span data-ttu-id="2f6cf-108">フォーム全体に署名する、またはフォーム内の署名可能な特定のデータ セットに個別に署名する。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-108">Enable signatures for the entire form, or for specific sets of data in the form that can be signed separately.</span></span>
    
- <span data-ttu-id="2f6cf-p101">署名対象にできる各データ セットについて、単一の署名または複数の署名が可能かどうかを指定し、その署名間の関係を指定する。たとえば、それらの署名を同等の連署にするのか、それとも新しい各署名を以前のすべての署名の副署にするのかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-p101">Specify, for each set of data that can be signed, whether a single signature or multiple signatures are allowed and what their relationship will be. For example, you can specify whether they are parallel co-signatures or whether each new signature countersigns all the earlier signatures.</span></span>
    
- <span data-ttu-id="2f6cf-111">ユーザーがフォームに署名したときにフォームに表示されるメッセージを指定する。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-111">Specify a message to be shown to form users as they sign the form.</span></span>
    
- <span data-ttu-id="2f6cf-112">文書に署名を挿入し、それを確認する。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-112">Insert and see a signature in the document.</span></span> 
    
- <span data-ttu-id="2f6cf-p102">セキュリティ向上のために各署名に追加された検証可能な非否認情報を確認する。この追加情報には、各署名者に表示されたフォームのビューが含まれています。この追加情報は署名の一部になっていて、署名を無効にすることなく削除することはできません。このデータは、フォーム内の署名をクリックして [ **デジタル署名の確認**] ダイアログ ボックスを表示することにより、いつでも再表示できます。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-p102">View verifiable non-repudiation information that has been added to each signature for increased security. This additional information, which includes a view of the form as it was presented to each signer, is part of the signature and cannot be removed without invalidating the signature. At any time, you can recall this data by clicking on the signature in the form to display the **Verify Digital Signature** dialog box.</span></span> 
    
- <span data-ttu-id="2f6cf-p103">デジタル署名の操作にオブジェクト モデルを活用する。デジタル署名のオブジェクト モデルを通じて、署名ブロックにカスタム情報を完全に信頼できる形で追加できます。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-p103">Take advantage of an object model for working with digital signatures. Add custom information to the signature block in fully trusted forms through the digital signature object model.</span></span> 
    
## <a name="overview-of-the-digital-signatures-object-model"></a><span data-ttu-id="2f6cf-118">デジタル署名のオブジェクト モデルの概要</span><span class="sxs-lookup"><span data-stu-id="2f6cf-118">Overview of the Digital Signatures Object Model</span></span>

### <a name="events"></a><span data-ttu-id="2f6cf-119">イベント</span><span class="sxs-lookup"><span data-stu-id="2f6cf-119">Events</span></span>

<span data-ttu-id="2f6cf-120">デジタル署名のオブジェクト モデルには、次のイベントがあります。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-120">The object model for digital signatures provides the following event.</span></span>
  
|<span data-ttu-id="2f6cf-121">**名前**</span><span class="sxs-lookup"><span data-stu-id="2f6cf-121">**Name**</span></span>|<span data-ttu-id="2f6cf-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="2f6cf-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f6cf-123">OnSign</span><span class="sxs-lookup"><span data-stu-id="2f6cf-123">OnSign</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |<span data-ttu-id="2f6cf-124">署名するための一連の署名データが選択されたときに発生します。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-124">Occurs after a set of signable data has been selected to sign.</span></span>  <br/> <span data-ttu-id="2f6cf-p104">このイベントを使用すると、デジタル署名に格納されているデータを操作することができます。たとえば、信頼されるタイムスタンプ サーバーからデータを追加したり、トランザクションのサーバー側副署名を追加したりできます。また、このイベントを使用すると、現在のユーザーが特定のグループのメンバーでない場合に署名を拒否することもできます。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-p104">You can use this event to manipulate the data stored within the digital signature. For example, you can add data from a trusted timestamp server, or add a server-side countersignature of the transaction. You can also use this event to block signing if the current user is not a member of a particular group.</span></span>  <br/> |
   
<span data-ttu-id="2f6cf-128">**OnSign** イベントは、 [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) オブジェクトへの参照を返します。このオブジェクトには、次のプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-128">The **OnSign** event returns a reference to the [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) object, which provides the following properties.</span></span> 
  
|<span data-ttu-id="2f6cf-129">**名前**</span><span class="sxs-lookup"><span data-stu-id="2f6cf-129">**Name**</span></span>|<span data-ttu-id="2f6cf-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="2f6cf-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f6cf-131">ReturnStatus</span><span class="sxs-lookup"><span data-stu-id="2f6cf-131">ReturnStatus</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |<span data-ttu-id="2f6cf-132">**OnSign** イベントから返された状態を示す **Boolean** 値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-132">Gets or sets a **Boolean** value indicating the return status of the **OnSign** event.</span></span>  <br/> |
|[<span data-ttu-id="2f6cf-133">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="2f6cf-133">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |<span data-ttu-id="2f6cf-134">**OnSign** イベントを発生させた署名済みデータ ブロックを取得します。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-134">Gets the signed data block that triggered the **OnSign** event.</span></span>  <br/> |
|[<span data-ttu-id="2f6cf-135">XDocument</span><span class="sxs-lookup"><span data-stu-id="2f6cf-135">XDocument</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |<span data-ttu-id="2f6cf-136">**OnSign** イベントに関連付けられている **XDocument** オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-136">Gets a reference to the **XDocument** object associated with the **OnSign** event.</span></span>  <br/> |
   
### <a name="collections-and-objects"></a><span data-ttu-id="2f6cf-137">コレクションおよびオブジェクト</span><span class="sxs-lookup"><span data-stu-id="2f6cf-137">Collections and Objects</span></span>

<span data-ttu-id="2f6cf-138">デジタル署名のオブジェクト モデルには、次のコレクションがあります。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-138">The object model for digital signatures provides the following collections.</span></span>
  
|<span data-ttu-id="2f6cf-139">**名前**</span><span class="sxs-lookup"><span data-stu-id="2f6cf-139">**Name**</span></span>|<span data-ttu-id="2f6cf-140">**説明**</span><span class="sxs-lookup"><span data-stu-id="2f6cf-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f6cf-141">SignedDataBlocksCollection</span><span class="sxs-lookup"><span data-stu-id="2f6cf-141">SignedDataBlocksCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |<span data-ttu-id="2f6cf-142">フォーム定義ファイル (.xsf) で定義されているフォーム テンプレート内の [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) オブジェクトのコレクション。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-142">The collection of the [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) objects in the form template as defined in the form definition file (.xsf).</span></span>  <br/> <span data-ttu-id="2f6cf-p105">**SignedDataBlocksCollection** コレクションには、フォームに関連付けられている **SignedDataBlockObjects** オブジェクトにアクセスするためのプロパティがあります。 **SignedDataBlocks** コレクションへのアクセスには、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) オブジェクトの [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) プロパティを使用します。  </span><span class="sxs-lookup"><span data-stu-id="2f6cf-p105">The **SignedDataBlocksCollection** collection implements properties that can be used to access the **SignedDataBlockObjects** objects associated with a form. The **SignedDataBlocks** collection is accessible through the [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) object.  </span></span><br/> |
|[<span data-ttu-id="2f6cf-145">SignaturesCollection</span><span class="sxs-lookup"><span data-stu-id="2f6cf-145">SignaturesCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |<span data-ttu-id="2f6cf-146">フォーム内の各 [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) に対する **SignatureObject** のコレクションが格納されています。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-146">Contains a collection of [SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) objects for each **SignedDataBlockObject** in the form.</span></span>  <br/> <span data-ttu-id="2f6cf-p106">**SignaturesCollection** コレクションには、フォームに関連付けられている **SignatureObject** オブジェクトへのアクセスや、署名の作成に使用できるプロパティとメソッドが実装されています。このコレクションには、 **SignedDataBlockObject** オブジェクトを通じてアクセスできます。  </span><span class="sxs-lookup"><span data-stu-id="2f6cf-p106">The **SignaturesCollection** collection implements properties and a method that can be used to access a form's associated **SignatureObject** objects and to create a signature. It is accessible through the **SignedDataBlockObject** object.  </span></span><br/> <span data-ttu-id="2f6cf-p107">[SignaturesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) コレクションの **Create** メソッドを使用する際には、 [SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) オブジェクトに対して **Sign** メソッドを呼び出すまでは署名が書き込まれないことを覚えておいてください。これらのメソッドは、完全に信頼されたフォーム テンプレートの **OnSign** イベント ハンドラーからしか呼び出せません。  </span><span class="sxs-lookup"><span data-stu-id="2f6cf-p107">When you use the [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) method of the **SignaturesCollection** collection, keep in mind that the signature is not written until the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) method is called on the **SignatureObject** object. These methods can be called only from the **OnSign** event handler of a fully trusted form template.  </span></span><br/> |
   
<span data-ttu-id="2f6cf-151">デジタル署名のオブジェクト モデルには、次のオブジェクトがあります。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-151">The object model for digital signatures provides the following objects.</span></span>
  
|<span data-ttu-id="2f6cf-152">**名前**</span><span class="sxs-lookup"><span data-stu-id="2f6cf-152">**Name**</span></span>|<span data-ttu-id="2f6cf-153">**説明**</span><span class="sxs-lookup"><span data-stu-id="2f6cf-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f6cf-154">SignedDataBlockObject</span><span class="sxs-lookup"><span data-stu-id="2f6cf-154">SignedDataBlockObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |<span data-ttu-id="2f6cf-p108">フォーム内の署名可能な一連のデータを表します。 **SignedDataBlock** オブジェクトには、署名可能なデータ セットをプログラムで操作するために使用できる多数のプロパティと 1 つのメソッドがあります。  </span><span class="sxs-lookup"><span data-stu-id="2f6cf-p108">Represents a set of signable data in a form. The **SignedDataBlock** object provides a number of properties and one method that can be used to programmatically interact with a set of signable data.  </span></span><br/> |
|[<span data-ttu-id="2f6cf-157">SignatureObject</span><span class="sxs-lookup"><span data-stu-id="2f6cf-157">SignatureObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |<span data-ttu-id="2f6cf-p109">フォームまたはフォーム内の署名可能な一連のデータに追加されたデジタル署名を表します。 **SignatureObject** コレクションには、デジタル署名に関する情報の取得に使用できる各プロパティ、および XML デジタル署名ブロックの書き込みとその暗号化ハッシュ値の計算のための [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) メソッドが実装されています。  </span><span class="sxs-lookup"><span data-stu-id="2f6cf-p109">Represents a digital signature that has been added to a form or set of signable data in a form. The **SignatureObject** collection implements properties that can be used to retrieve information about the digital signature, and the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) method for writing the XML digital signature block and computing its cryptographic hash value.  </span></span><br/> |
|[<span data-ttu-id="2f6cf-160">CertificateObject</span><span class="sxs-lookup"><span data-stu-id="2f6cf-160">CertificateObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |<span data-ttu-id="2f6cf-161">署名の作成に使用された X.509 デジタル証明書を表します。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-161">Represents the X.509 digital certificate that has been used to create the signature.</span></span>  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a><span data-ttu-id="2f6cf-162">プログラムでデジタル署名を操作する</span><span class="sxs-lookup"><span data-stu-id="2f6cf-162">Working with Digital Signatures Programmatically</span></span>

<span data-ttu-id="2f6cf-p110">InfoPath 2003 互換オブジェクト モデルには、デジタル署名をプログラムによって操作するための各種メンバーがあります。特に、完全に信頼されたフォームでは、次のようなタイムラインに従って、署名ブロックをコミットする前に署名ブロックにカスタム情報を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-p110">The InfoPath 2003-compatible object model provides members for interacting with digital signatures programmatically. In particular, fully-trusted forms can add custom information to the signature block before it is committed, according to the following timeline:</span></span>
  
1. <span data-ttu-id="2f6cf-165">ユーザーがフォームにデジタル署名を追加する操作を開始します。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-165">User chooses to add a digital signature to a form.</span></span>
    
2. <span data-ttu-id="2f6cf-166">[ **デジタル署名ウィザード**] の最初のパネルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-166">The first panel of the **Digital Signature Wizard** is displayed.</span></span> 
    
3. <span data-ttu-id="2f6cf-167">**SignedDataBlockObject** オブジェクトによって表された選択中のデータの **OnSign** イベントが発生し、 **SignedDataBlockObject** の **Sign** メソッドおよび **SignaturesCollection** コレクションの **Create** メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-167">The **OnSign** event for the selected data represented by the **SignedDataBlockObject** object is raised, and the **Sign** method of **SignedDataBlockObject** and the **Create** method of the **SignaturesCollection** collection are executed.</span></span> 
    
4. <span data-ttu-id="2f6cf-168">任意のオプション カスタム操作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-168">Any optional custom actions are executed.</span></span>
    
5. <span data-ttu-id="2f6cf-169">**SignatureObject** の **Sign** メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-169">The **Sign** method of the **SignatureObject** is executed.</span></span> 
    
6. <span data-ttu-id="2f6cf-170">署名に使用する証明書を選択するためのウィザードの 2 つ目のパネル、およびコメントを入力するための 3 つ目のパネルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-170">Second and third panes of the wizard are displayed for selecting a certificate to sign with and to enter comments.</span></span>
    
7. <span data-ttu-id="2f6cf-171">非否認情報が表示されます (この情報は、後から [ **デジタル署名の確認**] ダイアログ ボックスでも確認できます)。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-171">The non-repudiation information is displayed (which can be viewed later with the **Verify Digital Signature** dialog box).</span></span> 
    
8. <span data-ttu-id="2f6cf-172">[ **署名**] ボタンがクリックされると、そのフォーム用の署名のコレクションに署名が追加されます。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-172">When the **Sign** button is clicked, the signature is added to collection of signatures for the form.</span></span> 
    
<span data-ttu-id="2f6cf-173">次の例は、[ **署名**] ダイアログ ボックスを開いて、信頼できるタイムスタンプ サービスから取得したタイムスタンプ値で副署の署名を行います。</span><span class="sxs-lookup"><span data-stu-id="2f6cf-173">The following example invokes the **Sign** dialog box and countersigns the signature with a timestamp value retrieved from a trusted timestamp service.</span></span> 
  
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


