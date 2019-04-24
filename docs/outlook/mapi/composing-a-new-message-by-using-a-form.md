---
title: フォームを使用して新しいメッセージを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335127"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="9cc59-103">フォームを使用して新しいメッセージを作成する</span><span class="sxs-lookup"><span data-stu-id="9cc59-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="9cc59-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cc59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cc59-105">フォームを使用して新しいメッセージを作成するには、まず、新しいカスタムメッセージオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="9cc59-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="9cc59-106">**フォームを使用して新しいメッセージを作成するには**</span><span class="sxs-lookup"><span data-stu-id="9cc59-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="9cc59-107">フォームマネージャーの[imapiformmgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md)メソッドを呼び出して、フォーム情報オブジェクトへのポインターを取得します。これは、 [imapiformmgr: imapiprop](imapiforminfoimapiprop.md)インターフェイスを実装するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="9cc59-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="9cc59-108">[imapiformmgr:: CreateForm](imapiformmgr-createform.md)を呼び出して、フォーム情報オブジェクトへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="9cc59-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="9cc59-109">**CreateForm**は、適切なフォームサーバーを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="9cc59-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="9cc59-110">さらに、インターフェイス識別子を**CreateForm**に渡して、新しいメッセージへのアクセスに使用するインターフェイスを指定します。</span><span class="sxs-lookup"><span data-stu-id="9cc59-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="9cc59-111">通常、IID_IPersistMessage を**CreateForm**に渡すことによって、 [IPersistMessage: IUnknown](ipersistmessageiunknown.md)を要求します。</span><span class="sxs-lookup"><span data-stu-id="9cc59-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="9cc59-112">[IPersistMessage:: save](ipersistmessage-save.md)メソッドを呼び出して、新しいメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="9cc59-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="9cc59-113">フォームサーバーは、メッセージの作成時に、メッセージの必要なプロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cc59-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="9cc59-114">次の2つの方法のいずれかを使用してメッセージを読み込みます。 [imapiformmgr:: loadform](imapiformmgr-loadform.md)または[imapisession::P repareform](imapisession-prepareform.md)の後に[imapisession:: showform](imapisession-showform.md)を続けます。</span><span class="sxs-lookup"><span data-stu-id="9cc59-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="9cc59-115">これらの戦略の詳細については、「[フォームへのメッセージの読み込み](loading-a-message-into-a-form.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9cc59-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="9cc59-116">新しいカスタムメッセージをフォームサーバーに読み込むときに、**そのメッセージに必要な処理中にそのメッセージに関する情報を取得する機会が既にあるため、パフォーマンスが向上する可能性があります。ResolveMessageClass**および**CreateForm**呼び出し。</span><span class="sxs-lookup"><span data-stu-id="9cc59-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="9cc59-117">このため、「[メッセージをフォームに読み込む](loading-a-message-into-a-form.md)」で説明されているように、 **loadform**を呼び出す前に、必要な処理を簡素化できます。</span><span class="sxs-lookup"><span data-stu-id="9cc59-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

