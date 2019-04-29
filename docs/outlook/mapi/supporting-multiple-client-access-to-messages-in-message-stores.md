---
title: ���[���̕ۑ��ꏊ�ŕ����N���C�A���g�̃��b�Z�[�W�ւ̃A�N�Z�X��T�|�[�g
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 40bed9ccbe8073c8e9ea5176c9d4be8fe642b52d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439864"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a><span data-ttu-id="99e53-103">���[���̕ۑ��ꏊ�ŕ����N���C�A���g�̃��b�Z�[�W�ւ̃A�N�Z�X��T�|�[�g</span><span class="sxs-lookup"><span data-stu-id="99e53-103">Supporting Multiple Client Access to Messages in Message Stores</span></span>

  
  
<span data-ttu-id="99e53-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99e53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99e53-p101">It is possible for multiple client applications to open a given message simultaneously. Message store providers do not have to follow any particular rules for governing such access. However, if the client applications modify the message and save their changes, the store provider should comply with the following rules:</span><span class="sxs-lookup"><span data-stu-id="99e53-p101">It is possible for multiple client applications to open a given message simultaneously. Message store providers do not have to follow any particular rules for governing such access. However, if the client applications modify the message and save their changes, the store provider should comply with the following rules:</span></span>
  
- <span data-ttu-id="99e53-108">���b�Z�[�W��J���Ă���B��̃N���C�A���g�̏ꍇ�Ɠ��l�ɑ��s����[IMAPIProp::SaveChanges](imapiprop-savechanges.md)���\�b�h�̍ŏ��̌Ăяo��������܂��B</span><span class="sxs-lookup"><span data-stu-id="99e53-108">Allow the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to proceed as if it were the only client that has the message open.</span></span> 
    
- <span data-ttu-id="99e53-109">�㑱 **SaveChanges**�ʘb�𑼂̃N���C�A���g�ɂ���āA���b�Z�[�W �X�g�A �v���o�C�_�[���ύX�𖳎����AMAPI_E_OBJECT_CHANGED ��Ԃ��K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="99e53-109">On the subsequent **SaveChanges** calls by other clients, the message store provider should ignore the changes and return MAPI_E_OBJECT_CHANGED.</span></span> 
    
- <span data-ttu-id="99e53-p102">FORCE_SAVE �t���O������x **SaveChanges**�Ăяo���ɂ��AMAPI_E_OBJECT_CHANGED ���^�[�� �R�[�h�ɑΉ�����A�v���P�[�V�����ɃN���C�A���g��g�p�ł��܂��B�N���C�A���g �A�v���P�[�V�����ł́A���b�Z�[�W �X�g�A �v���o�C�_�[�́A�V�����ňȑO�̕ύX��u�������Ă��������B</span><span class="sxs-lookup"><span data-stu-id="99e53-p102">Allow client applications to respond to a MAPI_E_OBJECT_CHANGED return code by calling **SaveChanges** again with the FORCE_SAVE flag. If a client application does this, the message store provider should replace the previous changes with the new ones.</span></span> 
    
<span data-ttu-id="99e53-112">�܂��́A���b�Z�[�W �X�g�A �v���o�C�_�[�́A��������o���A���[�U�[���A���̃��b�Z�[�W��ێ�����A�V�����ύX] �ŁA���̃��b�Z�[�W��㏑������A�܂��͕ʂ̏ꏊ�ɕύX��ۑ����邩�ǂ�����I��ł���C���^�[�t�F�C�X��s�����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="99e53-112">Alternatively, the message store provider can detect the conflict and present an interface that enables the user to choose whether to keep the original message, overwrite the original message with the new changes, or save the new changes to another location.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="99e53-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="99e53-113">See also</span></span>



[<span data-ttu-id="99e53-114">メッセージ ストアのメッセージの実装</span><span class="sxs-lookup"><span data-stu-id="99e53-114">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

