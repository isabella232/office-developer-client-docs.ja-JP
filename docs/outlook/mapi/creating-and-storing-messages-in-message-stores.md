---
title: �쐬�ƃ��b�Z�[�W �X�g�A�Ń��b�Z�[�W��ۑ����܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 32cfae36fb519654c1fb92d2f3b688c966f9288f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799862"
---
# <a name="creating-and-storing-messages-in-message-stores"></a><span data-ttu-id="fead2-103">�쐬�ƃ��b�Z�[�W �X�g�A�Ń��b�Z�[�W��ۑ����܂��B</span><span class="sxs-lookup"><span data-stu-id="fead2-103">Creating and Storing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="fead2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fead2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fead2-p101">���b�Z�[�W �X�g�A �v���o�C�_�[��쐬���ċ@�\�L����Ƀ��b�Z�[�W��i�[������@�A��ɂȂ�L���惁�J�j�Y�����̂ɑ傫���ˑ����܂��B��ʂɁA���b�Z�[�W�Ƃ��̒l�̃v���p�e�B��ێ����邽�߂̃R�[�h��L�q�݂̂ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="fead2-p101">How your message store provider creates and stores messages in the underlying storage mechanism depends heavily on the underlying storage mechanism itself. In general, you need only to write code to preserve the properties of a message and their values.</span></span>
  
<span data-ttu-id="fead2-p102">���b�Z�[�W�̕ۑ����v���o�C�[�[�́A�V�������b�Z�[�W��쐬�A�v���o�C�](imapifolderimapicontainer.md)�[�́A���b�Z�[�W�̕K�v�ȃv���p�e�B���A���b�Z�[�W��쐬����K�v������܂��B�����̃v���p�e�B�̈ꗗ�̃h�L�������g�ɋL�ڂ���āA [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)�C���^�[�t�F�C�X�ł��B���̌�A�N���C�A���g �A�v���P�[�V������[IMAPIProp](imapipropiunknown.md)���@�ŁA�ǉ��̃v���p�e�B��ǉ����܂��B</span><span class="sxs-lookup"><span data-stu-id="fead2-p102">When the message store provider creates a new message, the provider needs to create the message with the required properties for messages. A list of these properties can be found in the documentation for the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. After that, client applications add any additional properties with [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
  
<span data-ttu-id="fead2-110">メッセージは、プロバイダーの保存、基になるストレージ機構にメッセージを保存、するとプロバイダーは、メッセージのプロパティを反復処理し、完全に復元できる場合は、メッセージを開いた後で、基になるストレージ機構に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fead2-110">When the message store provider saves a message to the underlying storage mechanism, the provider needs to iterate over the message's properties, and save them to the underlying storage mechanism such that they can be fully recovered if the message is later opened.</span></span>
  
<span data-ttu-id="fead2-111">MAPI が必要です[IMessage](imessageimapiprop.md)インターフェイスのプロパティは、トランザクション処理されている、ことそれらを変更しないになることは永続的なメッセージ オブジェクトの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されるまでを意味します。</span><span class="sxs-lookup"><span data-stu-id="fead2-111">MAPI requires that the properties on [IMessage](imessageimapiprop.md) interfaces are transacted, meaning that changes made to them do not become permanent until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called on the message object.</span></span> <span data-ttu-id="fead2-112">メッセージ ストア プロバイダーは、この動作を実装します。</span><span class="sxs-lookup"><span data-stu-id="fead2-112">The message store provider is responsible for implementing this behavior.</span></span> <span data-ttu-id="fead2-113">通常これは困難です。単にそれらを修正しているときに、メモリ内のプロパティを保持していると、**たいていは SaveChanges**が呼び出されたときに基になるストレージ機構に組み込むにも同じことを意味します。</span><span class="sxs-lookup"><span data-stu-id="fead2-113">Usually this is not difficult; it simply means holding properties in memory while they are being modified and committing them to the underlying storage mechanism when **SaveChanges** is called.</span></span> 
  
<span data-ttu-id="fead2-114">���b�Z�[�W�̃I�u�W�F�N�g�̈ꕔ�̃v���p�e�B�ł́A���̂悤�ɁA **SaveChanges**���\�b�h�Ɋ֘A����N���C�A���g �A�v���P�[�V�����ɓ��ʂȈӖ�������܂��B</span><span class="sxs-lookup"><span data-stu-id="fead2-114">Some properties on message objects have special semantics for client applications with respect to the **SaveChanges** method, as follows:</span></span> 
  
- <span data-ttu-id="fead2-115">**SaveChanges**が呼び出される前に、読み取り専用ですが、後で、いくつかのプロパティは読み取り/書き込みをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fead2-115">Some properties should be read/write before **SaveChanges** is called, but read-only afterward.</span></span> <span data-ttu-id="fead2-116">メッセージを作成し、読み取り/書き込み) をクライアント アプリケーションが**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) を最初に設定は、たとえば、 **savechanges メソッド**の最初の呼び出し後に変更することはできませんが。</span><span class="sxs-lookup"><span data-stu-id="fead2-116">For example, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) is set initially by the client application that creates the message (and thus is read/write) but cannot be changed after the first call to **SaveChanges**.</span></span>
    
- <span data-ttu-id="fead2-p105">�ꕔ�̃v���p�e�B�ł́A **IMAPIFolder**���@�ɂ́A[�t�H���_�[�̃v���p�e�B�ɓ��ʂ̊֌W������܂��B���Ƃ��΁A **PR_MESSAGE_FLAGS**�v���p�e�B��[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)�ʘb�Ɏg�p����t���O�Ɋ֘A���Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="fead2-p105">Some properties have special relations to properties on the folder they are in or to **IMAPIFolder** methods. For example, the **PR_MESSAGE_FLAGS** property is related to the flags used on the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) call.</span></span> 
    
- <span data-ttu-id="fead2-119">最初に**SaveChanges**が呼び出されるまで、いくつかプロパティを使用できません可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fead2-119">Some properties may not be available until **SaveChanges** is called for the first time.</span></span> <span data-ttu-id="fead2-120">たとえば、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) はできない場合があります**SaveChanges**が呼び出されるまでです。</span><span class="sxs-lookup"><span data-stu-id="fead2-120">For example, the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property may not be available until **SaveChanges** is called.</span></span> 
    
- <span data-ttu-id="fead2-121">いくつかのプロパティは、メッセージ オブジェクトの他のプロパティに特別な関係を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="fead2-121">Some properties can have special relationships to other properties on the message object.</span></span> <span data-ttu-id="fead2-122">たとえば、([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティは通常、リッチ テキスト形式のメッセージをサポートしているメッセージ ストア プロバイダーに、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティから派生します。</span><span class="sxs-lookup"><span data-stu-id="fead2-122">For example, the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property is usually derived from the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property in message store providers that support Rich Text Format messages.</span></span>
    
- <span data-ttu-id="fead2-123">いくつかのプロパティは、メッセージ ・ ストアに関連する複数のオブジェクトの種類によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="fead2-123">Some properties are used by more than one object type related to message stores.</span></span> <span data-ttu-id="fead2-124">たとえば、フォルダーおよびオブジェクトとメッセージ オブジェクトを格納するメッセージの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="fead2-124">For example, the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property is required on folder and message objects as well as message store objects.</span></span>
    
<span data-ttu-id="fead2-125">���̂悤�ȃv���p�e�B�̐������Z�}���e�B�N�X��������郁�b�Z�[�W �X�g�A �v���o�C�_�[�̐ӔC���邱�Ƃ�����߂��܂��B</span><span class="sxs-lookup"><span data-stu-id="fead2-125">It is the responsibility of the message store provider to implement the correct semantics for such properties.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fead2-126">�֘A����</span><span class="sxs-lookup"><span data-stu-id="fead2-126">See also</span></span>



<span data-ttu-id="fead2-127">[���[���̕ۑ��ꏊ�Ń��b�Z�[�W��������܂��B](implementing-messages-in-message-stores.md)</span><span class="sxs-lookup"><span data-stu-id="fead2-127">[Implementing Messages in Message Stores](implementing-messages-in-message-stores.md)</span></span>

