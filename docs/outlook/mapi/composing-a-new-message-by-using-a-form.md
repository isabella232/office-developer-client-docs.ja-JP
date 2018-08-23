---
title: フォームを使用した新しいメッセージの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f4b9cb00512838e6b54c0cc910b8f7279120db3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799802"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="b6a50-103">フォームを使用した新しいメッセージの作成</span><span class="sxs-lookup"><span data-stu-id="b6a50-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="b6a50-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6a50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6a50-105">フォームを使用して、新しいメッセージを作成するのには、まず、新しいカスタム メッセージ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="b6a50-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="b6a50-106">**フォームを使用して新しいメッセージを作成するには**</span><span class="sxs-lookup"><span data-stu-id="b6a50-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="b6a50-107">フォーム情報のオブジェクトへのポインターを取得するために、フォーム マネージャーの[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)メソッドを呼び出すなどを実装するオブジェクト、 [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="b6a50-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="b6a50-108">[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)への呼び出しで、フォームの情報オブジェクトへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="b6a50-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="b6a50-109">**CreateForm**は、フォームの適切なサーバーをロードします。</span><span class="sxs-lookup"><span data-stu-id="b6a50-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="b6a50-110">さらに、新しいメッセージへのアクセスに使用するインターフェイスを指定するのに**CreateForm**にインタ フェース識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="b6a50-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="b6a50-111">要求する通常は、 [IPersistMessage: IUnknown](ipersistmessageiunknown.md) **CreateForm**に IID_IPersistMessage を渡すことによって。</span><span class="sxs-lookup"><span data-stu-id="b6a50-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="b6a50-112">[IPersistMessage::Save](ipersistmessage-save.md)メソッドを呼び出して、新しいメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="b6a50-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="b6a50-113">フォーム サーバーは、メッセージを作成するときにメッセージの必要なプロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6a50-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="b6a50-114">2 つの方法のいずれかを使用して、メッセージの読み込み: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)または[IMAPISession::PrepareForm](imapisession-prepareform.md)の後に[IMAPISession::ShowForm](imapisession-showform.md)。</span><span class="sxs-lookup"><span data-stu-id="b6a50-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="b6a50-115">これらの方法の詳細については、[メッセージに、フォームの読み込み](loading-a-message-into-a-form.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6a50-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="b6a50-116">したがまだ機会があるメッセージについての情報を取得するため、フォームのサーバーに新しいカスタム メッセージを読み込むときにパフォーマンスの向上の機会があるなどのメッセージ クラス-、**に必要な処理中にResolveMessageClass**と**CreateForm**の呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="b6a50-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="b6a50-117">このため、[メッセージに、フォームの読み込み](loading-a-message-into-a-form.md)のトピックで説明する上で**LoadForm**を呼び出す前に必要な処理を簡略化することができます。</span><span class="sxs-lookup"><span data-stu-id="b6a50-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

