---
title: メッセージまたはフォルダーのコピーまたは移動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: '最終更新日: 2011 年11月8日'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413501"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="dc2d9-103">メッセージまたはフォルダーのコピーまたは移動</span><span class="sxs-lookup"><span data-stu-id="dc2d9-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="dc2d9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc2d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc2d9-105">クライアントは、次の4つの方法のいずれかを使用して、メッセージまたはフォルダーをコピーまたは移動できます。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="dc2d9-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="dc2d9-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="dc2d9-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="dc2d9-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="dc2d9-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="dc2d9-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="dc2d9-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="dc2d9-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="dc2d9-110">適切なフラグとパラメーターを設定することによって、 **CopyTo**および copyprops を**copyprops**や\*\*\*\* **copyprops**と同じように動作させることができます。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="dc2d9-111">呼び出すメソッドを決定するときは、以下の点を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="dc2d9-112">フォルダーまたはメッセージをコピーまたは移動していますか。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="dc2d9-113">移動またはコピーするフォルダーまたはメッセージについて、どのくらいの程度知っていますか。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="dc2d9-114">フォルダーまたはメッセージのプロパティの数はどれだけ移動またはコピーされますか。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="dc2d9-115">**imapiprop**メソッドを使用して、フォルダーまたはメッセージのいずれかをコピーまたは移動できます。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="dc2d9-116">**imapifolder:: copymessages**はメッセージのみを処理します。**imapifolder:: copyfolder**はフォルダーのみを使用します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="dc2d9-117">**imapifolder**メソッドを使用しても、コピーまたは移動するフォルダーやメッセージでサポートされているプロパティを認識する必要はありませんが、 **imapifolder**のメソッドを使用するには、いくつかの知識が必要です。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="dc2d9-118">**imapiprop:: copyprops**を使用すると、コピーまたは移動するフォルダーまたはメッセージのプロパティを明示的に指定できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="dc2d9-119">**imapiprop:: CopyTo**を使用すると、すべてのプロパティをコピーまたは移動するのでない限り、除外する必要があるものを明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="dc2d9-120">これらのメソッドの詳細については、「 [MAPI プロパティをコピー](copying-mapi-properties.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="dc2d9-121">コピーまたは移動するプロパティの数は、どのメソッドを使用するかによって決定に影響する場合があります。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="dc2d9-122">複数のメッセージをコピーまたは移動する場合は、 **imapifolder:: copymessages**を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="dc2d9-123">別の選択肢として、フォルダーの**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティのみをコピーするのには、 **imapiprop:: copyprops**を呼び出すことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="dc2d9-124">次の手順は、 **copymessages**の使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="dc2d9-125">1つまたは複数のメッセージをコピーまたは移動するには</span><span class="sxs-lookup"><span data-stu-id="dc2d9-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="dc2d9-126">コピー元とコピー先のフォルダーの有効なエントリ識別子を見つけます。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="dc2d9-127">これらのフォルダーを読み取り/書き込みモードで開くには、 [imapisession:: openentry](imapisession-openentry.md)または[IMsgStore:: openentry](imsgstore-openentry.md)を呼び出し、MAPI_MODIFY フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="dc2d9-128">**openentry**から返されるインターフェイスポインターが**imapifolder**インターフェイスポインターであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="dc2d9-129">含まれていない場合は、LPMAPIFOLDER 型にキャストします。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="dc2d9-130">コピーまたは移動する1つ以上のメッセージを表すエントリ識別子の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="dc2d9-131">次のフラグが設定された**copymessages:: imapifolder::** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="dc2d9-132">移動操作を実行する場合は、MESSAGE_MOVE。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="dc2d9-133">MESSAGE_DIALOG を使用して、フォルダーで進行状況インジケーターを表示する場合は、 _uluiparam_パラメーターでウィンドウハンドルを渡します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="dc2d9-134">コピー元とコピー先のフォルダーの**imapifolder**ポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="dc2d9-135">フォルダーの完全なコンテンツを別のフォルダーにコピーする場合は、ソースフォルダーの**imapifolder:: copyfolder**または**imapifolder:: CopyTo**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="dc2d9-136">いくつかのフォルダーのプロパティをコピーするには、 **imapiprop:: copyprops**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="dc2d9-137">フォルダーのプロパティの大部分をコピーするには、 **imapiprop:: CopyTo**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="dc2d9-138">たとえば、フォルダーの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) および**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) プロパティをコピーする場合は、次のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="dc2d9-139">**imapifolder:: copyfolder**を呼び出して、フォルダーのすべてのプロパティをコピーし、不要なものを新しいフォルダーから削除します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="dc2d9-140">**CopyTo**を呼び出して、 **PR_DISPLAY_NAME**と**PR_COMMENT**を除くすべてのフォルダーのプロパティを除外します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="dc2d9-141">**PR_DISPLAY_NAME**および**PR_COMMENT**を include 配列に渡して、呼び出し**copyprops**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="dc2d9-142">この場合、 **copyprops**は、一連のプロパティをコピーするために使用することを意図したものであり、実装するのに最も簡単な方法であるというのが最良の選択です。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="dc2d9-143">フォルダーのプロパティのみをコピーまたは移動するには、メッセージを含めずに、フォルダーの**imapiprop:: CopyTo**メソッドを呼び出し、次のプロパティを除外します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="dc2d9-144">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc2d9-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="dc2d9-145">**PR_FOLDER_ASSOCIATED_CONTENTS**([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dc2d9-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="dc2d9-146">copy メソッドは、S_OK を返すことができ、成功の合計、MAPI_W_PARTIAL_COMPLETION、部分的な成功、またはエラーを示します。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="dc2d9-147">MAPI_W_PARTIAL_COMPLETION が返された場合は、 **HR_FAILED**マクロを使用して、より具体的なエラーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="dc2d9-148">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="dc2d9-149">メッセージを別のメッセージストアにコピーし、Unicode を両方でサポートしていない場合は、コードページの変換によって情報が失われる可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="dc2d9-150">通常、メッセージストアが1つまたは両方の形式をサポートしているかどうかを知ることができないため、テキストプロパティを ASCII 文字列としてコピーするか、Unicode 文字列としてコピーするかを決定することはできません。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="dc2d9-151">unicode をサポートしている場合は、unicode コピーを実行してみてください。エラー値 MAPI_E_BAD_CHARWIDTH でエラーが発生した場合は、ASCII にします。</span><span class="sxs-lookup"><span data-stu-id="dc2d9-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

