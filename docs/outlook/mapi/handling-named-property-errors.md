---
title: 名前付きプロパティのエラーの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f6c12973a3ee2f9842e74f6f01b94553659dc1ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583310"
---
# <a name="handling-named-property-errors"></a><span data-ttu-id="3b178-103">名前付きプロパティのエラーの処理</span><span class="sxs-lookup"><span data-stu-id="3b178-103">Handling named property errors</span></span>
  
<span data-ttu-id="3b178-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b178-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b178-p101">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)�܂���[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)�傫�����鏈�����������悤�ɗv������ꍇ�A�G���[�l MAPI_E_TOO_BIG ���Ԃ���܂��B���M�҂ɉ�������K�v������܂��A�o�Ȉ˗��ɕ����A�������̈˗��A���[�v�œK�؂ȃ��\�b�h���܂��B</span><span class="sxs-lookup"><span data-stu-id="3b178-p101">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop.</span></span> 
  
<span data-ttu-id="3b178-107">�����I�Ȑ�������ƁA����̎��ʎq�ɑΉ��t���閼�O�͗v���ꍇ�ȂǁA1 �ȏ�̖��O�ŁA�Ăяo���̌��ʂ�������Ȃ��ꍇ�ɁA **GetNamesFromIDs**�� MAPI_W_ERRORS_RETURNED ��Ԃ��܂��B ���A�v���p�e�B�A�v���p�e�B�̃^�O�̔z��ŕs�����Ă���v���p�e�B�̃f�[�^�^�� PT_ERROR ��z�u���܂��B</span><span class="sxs-lookup"><span data-stu-id="3b178-107">When a call results in partial success, such as when the request is for names that map to specific identifiers and one or more names cannot be found, **GetNamesFromIDs** returns MAPI_W_ERRORS_RETURNED and places PT_ERROR in the property type for the missing property in the property tag array.</span></span> 
  
<span data-ttu-id="3b178-p102">�N���C�A���g�� **GetNamesFromIDs**�̓v���p�e�B����̂悤�ȕԂ���錋�ʂɌĂяo����s�����Ƃ�����܂������O�t���̂��ׂẴv���p�e�B�́A�t���O�ɂ���ď��O�̎�ނ��A�w�肵���v���p�e�B��ݒ肷��ɂ̓v���p�e�B���܂܂�Ă��Ȃ��ꍇ�ɂ��܂��B�N���C�A���g���T�[�r�X �v���o�C�_�[����߂邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="3b178-p102">Sometimes a client makes a call to **GetNamesFromIDs** that results in no properties being returned, such as when there are no properties in a specified property set, or when all named properties are of a type excluded by the flags. Clients can expect service providers to:</span></span> 
  
- <span data-ttu-id="3b178-110">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="3b178-110">Return S_OK.</span></span>
    
- <span data-ttu-id="3b178-111">�V���Ɋ��蓖�Ă�ꂽ�v���p�e�B �^�O�z��Ƀv���p�e�B �^�O�z��|�C���^�[�̓�e��ݒ肷��ɂ́A **cValues**�����o�[�� 0 �ɐݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="3b178-111">Set the contents of the property tag array pointer to a newly allocated property tag array with its **cValues** member set to zero.</span></span> 
    
- <span data-ttu-id="3b178-112">[MAPINAMEID](mapinameid.md)�\���̔z��̓�e�� NULL �ɐݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="3b178-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span></span> 
    
- <span data-ttu-id="3b178-113">0 �� **MAPINAMEID**�\���̐��̓�e��ݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="3b178-113">Set the contents of the count of **MAPINAMEID** structures to zero.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3b178-114">�֘A����</span><span class="sxs-lookup"><span data-stu-id="3b178-114">See also</span></span>

- [<span data-ttu-id="3b178-115">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="3b178-115">MAPI Named Properties</span></span>](mapi-named-properties.md)

