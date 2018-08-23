---
title: コピーまたはメッセージまたはフォルダーを移動します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: '最終更新日: 2011 年 11 月 8 日'
ms.openlocfilehash: 26fe135da93e0f5f94d9f7d264453b74f97a518b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799856"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="ebd01-103">コピーまたはメッセージまたはフォルダーを移動します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="ebd01-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ebd01-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ebd01-105">クライアントは、コピーまたはメッセージまたはフォルダーを移動する 4 つの方法のいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ebd01-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="ebd01-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="ebd01-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="ebd01-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ebd01-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="ebd01-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="ebd01-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="ebd01-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="ebd01-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="ebd01-110">適切なフラグとパラメーターを設定することにより**CopyTo**と**CopyProps**が動作するように**CopyFolder**または**CopyMessages**のようにします。</span><span class="sxs-lookup"><span data-stu-id="ebd01-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="ebd01-111">どのメソッドを呼び出すを決定する際に、次の問題を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="ebd01-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="ebd01-112">コピーまたは、フォルダーまたはメッセージを移動しますか。</span><span class="sxs-lookup"><span data-stu-id="ebd01-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="ebd01-113">どの程度ご存知のフォルダーまたはメッセージを移動またはコピーできるのですか。</span><span class="sxs-lookup"><span data-stu-id="ebd01-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="ebd01-114">フォルダーの数や、メッセージのプロパティを移動またはコピーされますか。</span><span class="sxs-lookup"><span data-stu-id="ebd01-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="ebd01-115">**IMAPIProp**メソッドは、コピーまたは移動するフォルダーまたはメッセージのいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ebd01-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="ebd01-116">**IMAPIFolder::CopyMessages**は、メッセージだけです。**IMAPIFolder::CopyFolder**は、フォルダーにのみで動作します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="ebd01-117">**IMAPIFolder**メソッドを使用してもフォルダーまたはメッセージをコピーまたは移動によってサポートされるプロパティのすべての知識が必要ありませんが、 **IMAPIProp**メソッドを使用するいくつかの知識が必要です。</span><span class="sxs-lookup"><span data-stu-id="ebd01-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="ebd01-118">**IMAPIProp::CopyProps**とのコピーまたは移動するフォルダーまたはメッセージのプロパティを明示的に指定できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ebd01-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="ebd01-119">**IMAPIProp::CopyTo**、コピーまたは移動するすべてのプロパティ、する場合を除き、明示的に指定してくださいどれを除外する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ebd01-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="ebd01-120">これらのメソッドの詳細については、 [MAPI プロパティのコピー](copying-mapi-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebd01-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="ebd01-121">コピーまたは移動するプロパティの数は、使用する方法の決定に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="ebd01-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="ebd01-122">コピーまたは複数のメッセージを移動する場合は、 **IMAPIFolder::CopyMessages**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="ebd01-123">代替の選択肢は、フォルダーの**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) のプロパティだけをコピーするのには**IMAPIProp::CopyProps**を呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="ebd01-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="ebd01-124">次の手順では、 **CopyMessages**を使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="ebd01-125">コピーまたは 1 つまたは複数のメッセージを移動するには</span><span class="sxs-lookup"><span data-stu-id="ebd01-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="ebd01-126">元とコピー先のフォルダーの有効なエントリの識別子を検索します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="ebd01-127">[IMAPISession::OpenEntry](imapisession-openentry.md)または[IMsgStore::OpenEntry](imsgstore-openentry.md)のいずれかを呼び出すと、MAPI_MODIFY フラグを設定して、読み取り/書き込みモードでこれらのフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="ebd01-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="ebd01-128">**OpenEntry**から返されたインターフェイス ポインターが**IMAPIFolder**インターフェイス ポインターであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="ebd01-129">いない場合は、LPMAPIFOLDER 型にキャストします。</span><span class="sxs-lookup"><span data-stu-id="ebd01-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="ebd01-130">コピーまたは移動する 1 つまたは複数のメッセージを表すエントリの識別子の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="ebd01-131">次のフラグのセットを使用して**IMAPIFolder::CopyMessages**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="ebd01-132">移動操作を実行する場合は、MESSAGE_MOVE です。</span><span class="sxs-lookup"><span data-stu-id="ebd01-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="ebd01-133">MESSAGE_DIALOG とウィンドウのパスは、 _ulUIParam_パラメーターに処理する場合は、進行状況インジケーターを表示するフォルダー。</span><span class="sxs-lookup"><span data-stu-id="ebd01-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="ebd01-134">元とコピー先のフォルダーの**IMAPIFolder**のポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="ebd01-135">別のフォルダーにフォルダーの内容全体をコピーする場合は、元のフォルダーの**IMAPIFolder::CopyFolder**または**IMAPIProp::CopyTo**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="ebd01-136">フォルダーのプロパティの一部をコピーするには、 **IMAPIProp::CopyProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="ebd01-137">ほとんどのフォルダーのプロパティをコピーするには、 **IMAPIProp::CopyTo**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="ebd01-138">たとえば、フォルダーの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) および**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) のプロパティをコピーする場合は、次のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="ebd01-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="ebd01-139">フォルダーのプロパティのすべてをコピーし、新しいフォルダーから不要なエントリを削除するのには**IMAPIFolder::CopyFolder**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="ebd01-140">**CopyTo**を呼び出すし、すべての**PR_DISPLAY_NAME**と**PR_COMMENT**以外のフォルダーのプロパティを除外します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="ebd01-141">**CopyProps**、 **PR_DISPLAY_NAME**と**PR_COMMENT**を含む配列に渡してを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="ebd01-142">この例では、 **CopyProps**に最適な選択肢小さいプロパティのセットをコピーするためにするものですのでを実装する最も簡単な呼び出し。</span><span class="sxs-lookup"><span data-stu-id="ebd01-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="ebd01-143">コピーまたはメッセージを含めずに、フォルダーのプロパティのみを移動、フォルダーの**IMAPIProp::CopyTo**メソッドを呼び出すし、次のプロパティを除外します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="ebd01-144">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ebd01-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="ebd01-145">**PR_FOLDER_ASSOCIATED_CONTENTS**([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ebd01-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="ebd01-146">コピー メソッドは S_OK を MAPI_W_PARTIAL_COMPLETION、完全な成功を示す部分的な成功またはエラーを示すを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="ebd01-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="ebd01-147">MAPI_W_PARTIAL_COMPLETION が返された場合より詳細なエラーにアクセスする**HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="ebd01-148">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebd01-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="ebd01-149">両方では、Unicode はサポートされていない別の 1 つのメッセージ ストアからメッセージをコピーする場合は、情報がコード ページ変換が失われることに注意します。</span><span class="sxs-lookup"><span data-stu-id="ebd01-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="ebd01-150">通常かわからないかどうか、メッセージ ・ ストアは、1 つまたは両方の形式をサポートとして ASCII 文字列または Unicode 文字列としてのテキストのプロパティをコピーするかどうかを判断することが不可能になります。</span><span class="sxs-lookup"><span data-stu-id="ebd01-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="ebd01-151">Unicode をサポートする場合は、実行しようと Unicode のコピーです。エラー値 MAPI_E_BAD_CHARWIDTH で失敗した場合、ASCII に頼る。</span><span class="sxs-lookup"><span data-stu-id="ebd01-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

