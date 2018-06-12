---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2bded946a1fc7d7ab181d3953defa24e247c003c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800756"
---
# <a name="imapisupportdosentmail"></a><span data-ttu-id="7d669-103">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="7d669-103">IMAPISupport::DoSentMail</span></span>

  
  
<span data-ttu-id="7d669-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d669-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d669-105">���M���ꂽ���b�Z�[�W��������܂��B</span><span class="sxs-lookup"><span data-stu-id="7d669-105">Processes a sent message.</span></span>
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="7d669-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="7d669-106">Parameters</span></span>

 <span data-ttu-id="7d669-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7d669-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7d669-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="7d669-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7d669-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="7d669-109">_lpMessage_</span></span>
  
> <span data-ttu-id="7d669-110">[����]�|�C���^�[��J���Ă��郁�b�Z�[�W�𑗐M�ς݃A�C�e����ۗ��Ɏw�肳��Ă���t�H���_�[�Ƀ��b�Z�[�W�𐶐�����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="7d669-110">[in] A pointer to the open message for which a message should be generated in the folder designated to hold sent items.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d669-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="7d669-111">Return value</span></span>

<span data-ttu-id="7d669-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d669-112">S_OK</span></span> 
  
> <span data-ttu-id="7d669-113">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="7d669-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d669-114">����</span><span class="sxs-lookup"><span data-stu-id="7d669-114">Remarks</span></span>

<span data-ttu-id="7d669-p101">���b�Z�[�W �X�g�A �v���o�C�**�[ �T�|�[�g �I�u�W�F�N�g�� **IMAPISupport::DoSentMail**���\�b�h��������܂��B���b�Z�[�W�̃X�g�A �v���o�C�**�[�́A���b�Z�[�W�̏���������������AMAPI �X�v�[���[�ŌĂяo�����[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)���\�b�h�̎������� [DoSentMail](imsgstore-finishedmsg.md)��Ăяo���܂��B **FinishedMsg**�́A���b�Z�[�W�̃��b�N�����A�ɂ��A���b�Z�[�W�̎Q�ƃJ�E���g�� 1�A **DoSentMail**��Ăяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="7d669-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span></span>
  
 <span data-ttu-id="7d669-118">**DoSentMail**�ł́A���̃^�X�N����s���܂��B</span><span class="sxs-lookup"><span data-stu-id="7d669-118">**DoSentMail** performs the following tasks:</span></span> 
  
- <span data-ttu-id="7d669-119">メッセージを送信した後、メッセージを削除する必要があるかどうかを判断するのには**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) のプロパティをチェックします。</span><span class="sxs-lookup"><span data-stu-id="7d669-119">Checks the message for the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to determine whether the message should be deleted after sending.</span></span>
    
- <span data-ttu-id="7d669-120">���M�ς݃A�C�e�� �t�H���_�[�̏ꏊ����肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="7d669-120">Determines the location of the Sent Items folder.</span></span>
    
- <span data-ttu-id="7d669-121">���b�Z�[�W�̂������M�ς݃A�C�e��] �ɐݒ肷��A�t�b�N�̏�����J�n���܂��B</span><span class="sxs-lookup"><span data-stu-id="7d669-121">Initiates message hook processing for any hooks set on the Sent Items folder.</span></span>
    
- <span data-ttu-id="7d669-122">送信済みアイテム フォルダー、削除済みアイテム フォルダー、または別のフォルダーにメッセージを移動します。</span><span class="sxs-lookup"><span data-stu-id="7d669-122">Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.</span></span>
    
- <span data-ttu-id="7d669-123">���b�Z�[�W�������܂��B</span><span class="sxs-lookup"><span data-stu-id="7d669-123">Releases the message.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d669-124">�֘A����</span><span class="sxs-lookup"><span data-stu-id="7d669-124">See also</span></span>



[<span data-ttu-id="7d669-125">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="7d669-125">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="7d669-126">PidTagDeleteAfterSubmit ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="7d669-126">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)
  
[<span data-ttu-id="7d669-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d669-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

