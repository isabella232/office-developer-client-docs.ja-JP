---
title: デジタル署名を操作する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- デジタル署名 [infopath 2007],InfoPath 2007,デジタル署名
localization_priority: Normal
ms.assetid: fd13fb71-aecf-47bb-8a6b-db70bd90ceeb
description: Microsoft.Office.InfoPath 名前空間のオブジェクト モデルには、プログラムによってデジタル署名を操作する機能が用意されています。
ms.openlocfilehash: ea657f80f6e38a06a91e19c245eadc203c7c580c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425576"
---
# <a name="work-with-digital-signatures"></a><span data-ttu-id="7ddf0-104">デジタル署名を操作する</span><span class="sxs-lookup"><span data-stu-id="7ddf0-104">Work with Digital Signatures</span></span>

<span data-ttu-id="7ddf0-105">[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間のオブジェクト モデルには、プログラムによってデジタル署名を操作する機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-105">The object model of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace provides features for working with digital signatures programmatically.</span></span> 
  
## <a name="digital-signature-features"></a><span data-ttu-id="7ddf0-106">デジタル署名の機能</span><span class="sxs-lookup"><span data-stu-id="7ddf0-106">Digital Signature Features</span></span>

<span data-ttu-id="7ddf0-107">InfoPath のデジタル署名機能を使用すると、以下の操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-107">The digital signatures features provided by InfoPath enable you to:</span></span> 
  
- <span data-ttu-id="7ddf0-108">フォーム全体に署名する、またはフォーム内の署名可能な特定のデータ セットに個別に署名する。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-108">Enable signatures for the entire form, or for specific sets of data in the form that can be signed separately.</span></span>
    
- <span data-ttu-id="7ddf0-p101">署名対象にできる各データ セットについて、単一の署名または複数の署名が可能かどうかを指定し、その署名間の関係を指定する。たとえば、それらの署名を同等の連署にするのか、それとも新しい各署名を以前のすべての署名の副署にするのかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-p101">Specify, for each set of data that can be signed, whether a single signature or multiple signatures are allowed and what their relationship will be. For example, you can specify whether they are parallel co-signatures or whether each new signature countersigns all the earlier signatures.</span></span>
    
- <span data-ttu-id="7ddf0-111">ユーザーがフォームに署名したときにフォームに表示されるメッセージを指定する。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-111">Specify a message to be shown to form users as they sign the form.</span></span>
    
- <span data-ttu-id="7ddf0-112">文書に署名を挿入し、それを確認する。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-112">Insert and see a signature in the document.</span></span> 
    
- <span data-ttu-id="7ddf0-p102">セキュリティ向上のために各署名に追加された検証可能な非否認情報を確認する。この追加情報には、各署名者に表示されたフォームのビューが含まれています。この追加情報は署名の一部になっていて、署名を無効にすることなく削除することはできません。このデータは、フォーム内の署名をクリックして [ **デジタル署名の確認**] ダイアログ ボックスを表示することにより、いつでも再表示できます。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-p102">View verifiable non-repudiation information that has been added to each signature for increased security. This additional information, which includes a view of the form as it was presented to each signer, is part of the signature and cannot be removed without invalidating the signature. At any time, you can recall this data by clicking on the signature in the form to display the **Verify Digital Signature** dialog box.</span></span> 
    
- <span data-ttu-id="7ddf0-p103">デジタル署名の操作にオブジェクト モデルを活用する。デジタル署名のオブジェクト モデルを通じて、署名ブロックにカスタム情報を完全に信頼できる形で追加できます。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-p103">Take advantage of an object model for working with digital signatures. Add custom information to the signature block in fully trusted forms through the digital signature object model.</span></span> 
    
## <a name="overview-of-the-digital-signatures-object-model"></a><span data-ttu-id="7ddf0-118">デジタル署名のオブジェクト モデルの概要</span><span class="sxs-lookup"><span data-stu-id="7ddf0-118">Overview of the Digital Signatures Object Model</span></span>

### <a name="the-sign-event"></a><span data-ttu-id="7ddf0-119">Sign イベント</span><span class="sxs-lookup"><span data-stu-id="7ddf0-119">The Sign Event</span></span>

<span data-ttu-id="7ddf0-120">デジタル署名のオブジェクト モデルには、次のイベントがあります。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-120">The object model for digital signatures provides the following event.</span></span>
  
|<span data-ttu-id="7ddf0-121">**名前**</span><span class="sxs-lookup"><span data-stu-id="7ddf0-121">**Name**</span></span>|<span data-ttu-id="7ddf0-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="7ddf0-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ddf0-123">Sign</span><span class="sxs-lookup"><span data-stu-id="7ddf0-123">Sign</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |<span data-ttu-id="7ddf0-124">署名するための一連のデータが選択されたときに発生します。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-124">Occurs after a set of data has been selected to sign.</span></span>  <br/> <span data-ttu-id="7ddf0-p104">このイベントを使用すると、デジタル署名に格納されているデータを操作することができます。たとえば、信頼されるタイムスタンプ サーバーからデータを追加したり、トランザクションのサーバー側副署名を追加したりできます。また、このイベントを使用すると、現在のユーザーが特定のグループのメンバーでない場合に署名を拒否することもできます。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-p104">You can use this event to manipulate the data stored within the digital signature. For example, you can add data from a trusted timestamp server, or add a server-side countersignature of the transaction. You can also use this event to block signing if the current user is not a member of a particular group.</span></span>  <br/> |
   
### <a name="the-signeventargs-object"></a><span data-ttu-id="7ddf0-128">SignEventArgs オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7ddf0-128">The SignEventArgs Object</span></span>

<span data-ttu-id="7ddf0-129">[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) イベントのイベント ハンドラーは、 [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) イベント オブジェクトで動作します。このイベント オブジェクトには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-129">An event handler for the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event can work with the [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) event object, which provides the following properties.</span></span> 
  
|<span data-ttu-id="7ddf0-130">**名前**</span><span class="sxs-lookup"><span data-stu-id="7ddf0-130">**Name**</span></span>|<span data-ttu-id="7ddf0-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="7ddf0-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ddf0-132">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="7ddf0-132">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |<span data-ttu-id="7ddf0-133">[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) イベントを発生させたデータのセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-133">Gets the set of data that raised the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event.</span></span>  <br/> |
|[<span data-ttu-id="7ddf0-134">SignatureWizard</span><span class="sxs-lookup"><span data-stu-id="7ddf0-134">SignatureWizard</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |<span data-ttu-id="7ddf0-135">[ **デジタル署名**] ダイアログ ボックスを表示するかどうかを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-135">Gets or sets whether to display the **Digital Signatures** dialog box.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="7ddf0-p105">InfoPath 2003 に付属している [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) マネージ コード オブジェクト モデルで、 [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) イベントの [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) イベント オブジェクトには、イベントに関連付けられているフォームの **XDocument** オブジェクトにアクセスするための **XDocument** プロパティがあります。このプロパティは、InfoPath Forms Services または InfoPath で [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) オブジェクト モデルを使用して作成されたフォーム テンプレートでは必要ありません。 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) クラスのオブジェクト モデル メンバーは、フォーム コード内で **this** (C# の場合) キーワードまたは **Me** (Visual Basic の場合) キーワードを使用してアクセスできるからです。たとえば、 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) クラスの [Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティにアクセスして、フォームが署名されているかどうかを判別するには、  `this.Signed` または  `Me.Signed.` を入力できます。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-p105">In the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) managed code object model that shipped with InfoPath 2003, the [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) event object for the [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) event provides an **XDocument** property for accessing the **XDocument** object of the form associated with the event. This is not necessary with form templates created with InfoPath Forms Services or InfoPath using the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) object model because the object model members of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class can be accessed in form code using the **this** (C#) or **Me** (Visual Basic) keyword. For example, to access the [Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class to determine if a form is signed, you can type either  `this.Signed` or  `Me.Signed.`</span></span>
  
### <a name="collections-and-objects"></a><span data-ttu-id="7ddf0-139">コレクションおよびオブジェクト</span><span class="sxs-lookup"><span data-stu-id="7ddf0-139">Collections and Objects</span></span>

<span data-ttu-id="7ddf0-140">デジタル署名のオブジェクト モデルには、次のコレクションがあります。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-140">The object model for digital signatures provides the following collections.</span></span>
  
|<span data-ttu-id="7ddf0-141">**名前**</span><span class="sxs-lookup"><span data-stu-id="7ddf0-141">**Name**</span></span>|<span data-ttu-id="7ddf0-142">**説明**</span><span class="sxs-lookup"><span data-stu-id="7ddf0-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ddf0-143">SignedDataBlockCollection</span><span class="sxs-lookup"><span data-stu-id="7ddf0-143">SignedDataBlockCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |<span data-ttu-id="7ddf0-144">InfoPath のデザイン モードでデザイン時に定義されたフォーム テンプレート内の [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) オブジェクトのコレクション。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-144">The collection of the [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) objects in the form template as defined at design time in InfoPath design mode.</span></span>  <br/> <span data-ttu-id="7ddf0-p106">[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) コレクションは、フォームに関連付けられている [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) オブジェクトへのアクセスに使用できるプロパティを実装しています。フォームに関連付けられている [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) オブジェクトは、 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) クラスの [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティを使用してアクセスできます。  </span><span class="sxs-lookup"><span data-stu-id="7ddf0-p106">The [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) collection implements properties that can be used to access the [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) objects associated with a form. The [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) object associated with a form is accessible through the [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.  </span></span><br/> |
|[<span data-ttu-id="7ddf0-147">SignatureCollection</span><span class="sxs-lookup"><span data-stu-id="7ddf0-147">SignatureCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |<span data-ttu-id="7ddf0-148">フォーム内の各 [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) オブジェクトの [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) オブジェクトのコレクションが格納されています。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-148">Contains a collection of [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) objects for each [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object in the form.</span></span>  <br/> <span data-ttu-id="7ddf0-p107">[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) クラスには、フォームに関連付けられている [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) オブジェクトへのアクセスや、署名の作成に使用できるプロパティとメソッドが実装されています。 [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) に関連付けられている [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) オブジェクトは、 [Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) プロパティを使用してアクセスできます。  </span><span class="sxs-lookup"><span data-stu-id="7ddf0-p107">The [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) class implements properties and a method that can be used to access a form's associated [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) objects and to create a signature. The [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) object associated with a [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) is accessible using the [Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) property.  </span></span><br/> <span data-ttu-id="7ddf0-p108">[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) クラスの [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) メソッドを使用するときは、 [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) オブジェクトに対して [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) メソッドを呼び出すまでは署名が書き込まれないことを覚えておいてください。これらのメソッドは、完全に信頼されたフォーム テンプレートの **Sign** イベント ハンドラーからしか呼び出せません。  </span><span class="sxs-lookup"><span data-stu-id="7ddf0-p108">When you use the [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) method of the [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) class, keep in mind that the signature is not written until the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) method is called on the [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) object. These methods can be called only from the **Sign** event handler of a fully trusted form template.  </span></span><br/> |
   
<span data-ttu-id="7ddf0-153">デジタル署名のオブジェクト モデルには、次のオブジェクトがあります。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-153">The object model for digital signatures provides the following objects.</span></span>
  
|<span data-ttu-id="7ddf0-154">**名前**</span><span class="sxs-lookup"><span data-stu-id="7ddf0-154">**Name**</span></span>|<span data-ttu-id="7ddf0-155">**説明**</span><span class="sxs-lookup"><span data-stu-id="7ddf0-155">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ddf0-156">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="7ddf0-156">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |<span data-ttu-id="7ddf0-p109">フォーム内の署名可能な一連のデータを表します。[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) オブジェクトには、署名可能なデータ セットをプログラムで操作するために使用できる多数のプロパティと 1 つのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-p109">Represents a set of signable data in a form. The [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object provides a number of properties and one method that can be used to programmatically interact with a set of signable data.  </span></span><br/> |
|[<span data-ttu-id="7ddf0-159">Signature</span><span class="sxs-lookup"><span data-stu-id="7ddf0-159">Signature</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |<span data-ttu-id="7ddf0-p110">フォームまたはフォーム内の署名可能な一連のデータに追加されたデジタル署名を表します。[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) オブジェクトには、デジタル署名に関する情報の取得に使用できる各プロパティ、および XML デジタル署名ブロックの書き込みとその暗号化ハッシュ値の計算のための [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) メソッドが実装されています。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-p110">Represents a digital signature that has been added to a form or set of signable data in a form. The [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) object implements properties that can be used to retrieve information about the digital signature, and the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) method for writing the XML digital signature block and computing its cryptographic hash value.  </span></span><br/> |
|[<span data-ttu-id="7ddf0-162">Certificate</span><span class="sxs-lookup"><span data-stu-id="7ddf0-162">Certificate</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |<span data-ttu-id="7ddf0-163">署名の作成に使用された X.509 デジタル証明書を表します。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-163">Represents the X.509 digital certificate that has been used to create the signature.</span></span>  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a><span data-ttu-id="7ddf0-164">プログラムでデジタル署名を操作する</span><span class="sxs-lookup"><span data-stu-id="7ddf0-164">Working with Digital Signatures Programmatically</span></span>

<span data-ttu-id="7ddf0-p111">[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間のオブジェクト モデルには、デジタル署名をプログラムによって操作するためのメンバーが用意されています。特に、完全に信頼されたフォームでは、次のようなタイムラインに従って、署名ブロックをコミットする前に署名ブロックにカスタム情報を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-p111">The object model of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace provides members for interacting with digital signatures programmatically. In particular, fully-trusted forms can add custom information to the signature block before it is committed, according to the following timeline:</span></span> 
  
1. <span data-ttu-id="7ddf0-167">ユーザーがフォームにデジタル署名を追加する操作を開始します。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-167">User chooses to add a digital signature to a form.</span></span>
    
2. <span data-ttu-id="7ddf0-168">[ **デジタル署名**] ダイアログ ボックスが表示され、ユーザーは [ **追加**] をクリックし、署名するデータを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-168">The **Digital Signatures** dialog box is displayed, the user clicks **Add**, and then selects the data to sign.</span></span>
    
3. <span data-ttu-id="7ddf0-169">[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) オブジェクトによって表されている選択されたデータの [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) イベントが発生し、 [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) オブジェクトの [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) メソッドおよび [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) コレクションの [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-169">The [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event for the selected data represented by the [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object is raised, and the [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) method of [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object and the [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) method of the [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) collection are executed.</span></span> 
    
4. <span data-ttu-id="7ddf0-170">任意のオプション カスタム操作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-170">Any optional custom actions are executed.</span></span>
    
5. <span data-ttu-id="7ddf0-171">[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) オブジェクトの [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-171">The [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) method of the [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) object is executed.</span></span> 
    
6. <span data-ttu-id="7ddf0-172">名前の入力 (または署名画像の選択)、署名に使用する証明書の選択、およびコメントの入力を行うための [ **署名**] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-172">The **Sign** dialog box is displayed for typing a name (or selecting a signature image), selecting a certificate to sign with, and to enter comments.</span></span> 
    
7. <span data-ttu-id="7ddf0-173">[ **署名**] ボタンがクリックされると、そのフォーム用の署名のコレクションに署名が追加され、非否認情報がキャプチャされて署名と共に保存されます (非否認情報は、後で [ **デジタル署名**] ダイアログ ボックスの [ **署名済みフォームの表示**] をクリックし、[ **収集された追加署名情報の表示**] をクリックすることで確認できます)。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-173">When the **Sign** button is clicked, the signature is added to the collection of signatures for the form and the non-repudiation information is captured and saved with the signature (which can be viewed later by clicking **View Signed Form** on the **Digital Signatures** dialog box, and then clicking **See the additional signing information that was collected**).</span></span>
    
<span data-ttu-id="7ddf0-174">次の例では、ユーザーが、選択されたデータの署名と、信頼できるタイムスタンプ サービスから取得したタイムスタンプ値で副署の署名を行うとき、[Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ddf0-174">The following example invokes the [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) method when the user signs the selected data and countersigns the signature with a timestamp value retrieved from a trusted timestamp service.</span></span> 
  
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


