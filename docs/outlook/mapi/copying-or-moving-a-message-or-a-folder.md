---
title: メッセージまたはフォルダーのコピーまたは移動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: '最終更新日: 2011 年 11 月 08 日'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413501"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="001c5-103">メッセージまたはフォルダーのコピーまたは移動</span><span class="sxs-lookup"><span data-stu-id="001c5-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="001c5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="001c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="001c5-105">クライアントは、次の 4 つの方法のいずれかを使用して、メッセージまたはフォルダーをコピーまたは移動できます。</span><span class="sxs-lookup"><span data-stu-id="001c5-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="001c5-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="001c5-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="001c5-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="001c5-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="001c5-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="001c5-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="001c5-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="001c5-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="001c5-110">適切なフラグとパラメーターを設定することで **、CopyTo** と **CopyProps** を **CopyFolder** や CopyMessages と同じ方法 **で動作できます**。</span><span class="sxs-lookup"><span data-stu-id="001c5-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="001c5-111">呼び出すメソッドを決定する際には、次の問題を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="001c5-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="001c5-112">フォルダーまたはメッセージをコピーまたは移動していますか?</span><span class="sxs-lookup"><span data-stu-id="001c5-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="001c5-113">移動またはコピーするフォルダーまたはメッセージについてどのくらい知っていますか?</span><span class="sxs-lookup"><span data-stu-id="001c5-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="001c5-114">移動またはコピーされるフォルダーまたはメッセージのプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="001c5-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="001c5-115">**IMAPIProp** メソッドを使用して、フォルダーまたはメッセージをコピーまたは移動できます。</span><span class="sxs-lookup"><span data-stu-id="001c5-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="001c5-116">**IMAPIFolder::CopyMessages はメッセージ** でのみ動作します。 **IMAPIFolder::CopyFolder は** フォルダーでのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="001c5-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="001c5-117">**IMAPIFolder** メソッドを使用しても、コピーまたは移動するフォルダーまたはメッセージでサポートされるプロパティに関する知識は必要ないのに対し **、IMAPIProp** メソッドを使用するにはいくつかの知識が必要です。</span><span class="sxs-lookup"><span data-stu-id="001c5-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="001c5-118">**IMAPIProp::CopyProps** では、コピーまたは移動するフォルダーまたはメッセージのプロパティを明示的に指定できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="001c5-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="001c5-119">**IMAPIProp::CopyTo** では、すべてのプロパティをコピーまたは移動する場合を除き、除外するプロパティを明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="001c5-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="001c5-120">これらのメソッドの詳細については [、「COPYing MAPI プロパティ」を参照してください](copying-mapi-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="001c5-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="001c5-121">コピーまたは移動するプロパティの数は、使用するメソッドに関する決定に影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="001c5-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="001c5-122">複数のメッセージをコピーまたは移動する場合は **、IMAPIFolder::CopyMessages を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="001c5-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="001c5-123">別の選択肢として **、IMAPIProp::CopyProps** を呼び出して、フォルダーのプロパティ [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)プロパティPR_CONTAINER_CONTENTSのみをコピーします。</span><span class="sxs-lookup"><span data-stu-id="001c5-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="001c5-124">次の手順は **、CopyMessages を使用する方法を示しています**。</span><span class="sxs-lookup"><span data-stu-id="001c5-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="001c5-125">1 つ以上のメッセージをコピーまたは移動するには</span><span class="sxs-lookup"><span data-stu-id="001c5-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="001c5-126">ソース フォルダーと移動先フォルダーの有効なエントリ識別子を見つける。</span><span class="sxs-lookup"><span data-stu-id="001c5-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="001c5-127">[IMAPISession::OpenEntry](imapisession-openentry.md)または[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出し、MAPI_MODIFY フラグを設定して、これらのフォルダーを読み取り/書き込みモードで開きます。</span><span class="sxs-lookup"><span data-stu-id="001c5-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="001c5-128">**OpenEntry** から返されるインターフェイス ポインターが **IMAPIFolder インターフェイス ポインターである必要** があります。</span><span class="sxs-lookup"><span data-stu-id="001c5-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="001c5-129">指定しない場合は、LPMAPIFOLDER 型にキャストします。</span><span class="sxs-lookup"><span data-stu-id="001c5-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="001c5-130">コピーまたは移動する 1 つ以上のメッセージを表すエントリ識別子の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="001c5-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="001c5-131">次 **のフラグを設定して IMAPIFolder::CopyMessages** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="001c5-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="001c5-132">MESSAGE_MOVE操作を実行する場合は、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="001c5-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="001c5-133">MESSAGE_DIALOG進行状況インジケーターを表示する場合は  _、ulUIParam_ パラメーターでウィンドウ ハンドルを取得して渡します。</span><span class="sxs-lookup"><span data-stu-id="001c5-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="001c5-134">ソース フォルダー **と移動先フォルダーの IMAPIFolder** ポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="001c5-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="001c5-135">フォルダーの完全な内容を別のフォルダーにコピーする場合は、ソース フォルダーの **IMAPIFolder::CopyFolder** または **IMAPIProp::CopyTo** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="001c5-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="001c5-136">フォルダーのプロパティの一部をコピーするには **、IMAPIProp::CopyProps メソッドを呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="001c5-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="001c5-137">フォルダーのプロパティのほとんどをコピーするには **、IMAPIProp::CopyTo を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="001c5-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="001c5-138">たとえば、フォルダーの **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティと PR_COMMENT ([PidTagComment](pidtagcomment-canonical-property.md)) プロパティをコピーする場合、次のオプションがあります。 </span><span class="sxs-lookup"><span data-stu-id="001c5-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="001c5-139">**IMAPIFolder::CopyFolder** を呼び出して、すべてのフォルダー プロパティをコピーし、新しいフォルダーから不要なプロパティを削除します。</span><span class="sxs-lookup"><span data-stu-id="001c5-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="001c5-140">**CopyTo を呼び** 出し、フォルダーとフォルダーのプロパティを除くすべてのPR_DISPLAY_NAME **を** PR_COMMENT。</span><span class="sxs-lookup"><span data-stu-id="001c5-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="001c5-141">**CopyProps を呼** び出し、include **PR_DISPLAY_NAME\*\*\*\*内PR_COMMENT** を渡します。</span><span class="sxs-lookup"><span data-stu-id="001c5-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="001c5-142">この場合、プロパティの小さなセットをコピーするために使用することを意図し、実装する最も簡単な呼び出しなので **、CopyProps** が最適です。</span><span class="sxs-lookup"><span data-stu-id="001c5-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="001c5-143">メッセージを含めずにフォルダー プロパティのみをコピーまたは移動するには、フォルダーの **IMAPIProp::CopyTo** メソッドを呼び出し、次のプロパティを除外します。</span><span class="sxs-lookup"><span data-stu-id="001c5-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="001c5-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="001c5-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="001c5-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="001c5-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="001c5-146">copy メソッドは、成功、成功S_OK、部分的な成功MAPI_W_PARTIAL_COMPLETIONエラーを示すデータを返します。</span><span class="sxs-lookup"><span data-stu-id="001c5-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="001c5-147">エラー MAPI_W_PARTIAL_COMPLETION場合は、HR_FAILED **マクロを** 使用して、より具体的なエラーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="001c5-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="001c5-148">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="001c5-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="001c5-149">あるメッセージ ストアから別のメッセージ ストアにメッセージをコピーし、Unicode が両方でサポートされていない場合は、コード ページ変換によって情報が失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="001c5-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="001c5-150">通常、メッセージ ストアが一方または両方の形式をサポートするかどうかはわかりません。そのため、テキスト プロパティを ASCII 文字列としてコピーするか、Unicode 文字列としてコピーするかは判断できません。</span><span class="sxs-lookup"><span data-stu-id="001c5-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="001c5-151">Unicode をサポートしている場合は、Unicode コピーを実行してみてください。エラー値を使用してエラーが発生した場合MAPI_E_BAD_CHARWIDTH ASCII を使用します。</span><span class="sxs-lookup"><span data-stu-id="001c5-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

