---
title: IPropDataHrGetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrGetPropAccess
api_type:
- COM
ms.assetid: 0101d291-00ca-4f66-b857-75d74b9f91a1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8441a4898659a5cd278265cb0199bb9097244aa3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801140"
---
# <a name="ipropdatahrgetpropaccess"></a><span data-ttu-id="6a0c4-103">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="6a0c4-103">IPropData::HrGetPropAccess</span></span>

  
  
<span data-ttu-id="6a0c4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6a0c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6a0c4-105">�A�N�Z�X ���x���� 1 �܂��͕����̃I�u�W�F�N�g�̃v���p�e�B�̏�Ԃ�擾���܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-105">Retrieves the access level and status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="6a0c4-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="6a0c4-106">Parameters</span></span>

 <span data-ttu-id="6a0c4-107">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="6a0c4-107">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="6a0c4-p101">[�\`�F�b�N �A�E�g]�A�N�Z�X ���x���ƃX�e�[�^�X��擾���邽�߂̃v���p�e�B������v���p�e�B �^�O�̔z��̓��͂���ȊO�̏ꍇ�A�|�C���^�[�� NULL ���� **HrGetPropAccess**�ɂ́A�A�N�Z�X ���x���Ƃ��ׂẴv���p�e�B�̏�Ԃ�擾����K�v������܂��B �o�͂ł́A�ǂ̃A�N�Z�X�ƃX�e�[�^�X�̃t���O�̃v���p�e�B�̃^�O�̔z�񂪎擾����܂����B�t���O�� _lprgulAccess_�p�����[�^�[��w���z��Ɋi�[����܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-p101">[in, out] On input, an array of property tags that indicate the properties for which to retrieve access levels and status; otherwise, a pointer to NULL, which indicates that **HrGetPropAccess** should retrieve access levels and status for all properties. On output, an array of property tags for which access and status flags were retrieved. The flags are stored in the array pointed to by the  _lprgulAccess_ parameter.</span></span> 
    
 <span data-ttu-id="6a0c4-111">_lprgulAccess_</span><span class="sxs-lookup"><span data-stu-id="6a0c4-111">_lprgulAccess_</span></span>
  
> <span data-ttu-id="6a0c4-p102">[�o��]�t���O �r�b�g�}�X�N�̔z��ւ̃|�C���^�[�B�e�r�b�g�́A�A�N�Z�X ���x�����]�A�܂��͂��̗����� _lpPropTagArray_�p�����[�^�[��w���A�z���̓���̃v���p�e�B���\������܂��B2 �̔z��A�ʒu _lprgulAccess_�|�C���g��̍ŏ��̃v���p�e�B�Ő������ŏ��̃r�b�g���� _lpPropTagArray_�|�C���g�Ȃǂł��B �v���p�e�B�̃^�O���ƂɁA���̃t���O��ݒ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-p102">[out] A pointer to an array of flag bitmasks. Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array pointed to by the  _lpPropTagArray_ parameter. The two arrays are positional in that the first bitmask that  _lprgulAccess_ points to describes the first property that  _lpPropTagArray_ points to, and so on. For each property tag, the following flags can be set:</span></span> 
    
|<span data-ttu-id="6a0c4-116">**�A�N�Z�X ���x���̃t���O**</span><span class="sxs-lookup"><span data-stu-id="6a0c4-116">**Access-level flag**</span></span>|<span data-ttu-id="6a0c4-117">**�t���O�̏��**</span><span class="sxs-lookup"><span data-stu-id="6a0c4-117">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6a0c4-118">IPROP_READONLY �v���p�e�B��ύX�ł��Ȃ����Ƃ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-118">IPROP_READONLY, which indicates that the property cannot be modified.</span></span>  <br/> |<span data-ttu-id="6a0c4-119">IPROP_CLEAN �v���p�e�B���ύX����Ă��Ȃ����Ƃ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-119">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="6a0c4-120">IPROP_READWRITE �v���p�e�B��ύX�ł��邱�Ƃ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-120">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="6a0c4-121">IPROP_DIRTY �v���p�e�B���ύX����Ă��邱�Ƃ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-121">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="6a0c4-122">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6a0c4-122">Return value</span></span>

<span data-ttu-id="6a0c4-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a0c4-123">S_OK</span></span> 
  
> <span data-ttu-id="6a0c4-124">�v���p�e�B�̃A�N�Z�X ���x���Ə�ԃt���O������ɕԂ���܂���B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-124">The access level and status flags for the properties were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a0c4-125">����</span><span class="sxs-lookup"><span data-stu-id="6a0c4-125">Remarks</span></span>

<span data-ttu-id="6a0c4-126">**IPropData::HrGetPropAccess**���\�b�h�́A�A�N�Z�X ���x���� 1 �ȏ�̃v���p�e�B�̏�Ԃ�����t���O�̐ݒ��擾���܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-126">The **IPropData::HrGetPropAccess** method retrieves a set of flags that indicates the access level and status for one or more properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6a0c4-127">呼び出し元へのメモ:</span><span class="sxs-lookup"><span data-stu-id="6a0c4-127">Notes to callers:</span></span>

<span data-ttu-id="6a0c4-128">**HrGetPropAccess**��́A���̖ړI�Ŏg�p�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-128">You can use **HrGetPropAccess** for the following purposes:</span></span> 
  
- <span data-ttu-id="6a0c4-129">�N���C�A���g���ύX���ꂽ�܂��͏������݉\�ȃv���p�e�B��폜���邩�ǂ�����m�F���܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-129">To determine whether a client changed or deleted a writable property.</span></span>
    
- <span data-ttu-id="6a0c4-130">�N���C�A���g��ύX����[IMAPIProp](imapipropiunknown.md)���\�b�h��g�p���ăv���p�e�B��폜�ł��Ȃ��悤�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-130">To prevent a client from changing or deleting a property by using the [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
    
<span data-ttu-id="6a0c4-p103">_lppPropTagArray_��w���v���p�e�B �^�O�z���̃v���p�e�B�̂����ꂩ���폜����Ă���ꍇ�́A **HrGetPropAccess**�́A�o�͂� 0 �ɔz��̃G���g����ݒ肵�܂��B _lppPropTagArray_�� NULL �ɐݒ肵�āA�I�u�W�F�N�g�̃v���p�e�B�̂����ꂩ���폜����Ă���A�z��ŁA�폜�����v���p�e�B���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-p103">If one of the properties in the property tag array pointed to by  _lppPropTagArray_ has been deleted, **HrGetPropAccess** sets the array entry to 0 on output. If you set  _lppPropTagArray_ to NULL and one of the object's properties has been deleted, the deleted property is returned in the array.</span></span> 
  
<span data-ttu-id="6a0c4-p104">�v���p�e�B���ύX����Ă���ꍇ�A���� IPROP_DIRTY �Ƀt���O���ݒ�z��̑Ή�����G���g���� _lprgulAccess_�|�C���g���܂��BIPROP_READONLY �� IPROP_READWRITE �ɐݒ肳��܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-p104">If a property has been modified, its IPROP_DIRTY flag is set in the corresponding entry in the array that  _lprgulAccess_ points to. Neither IPROP_READONLY nor IPROP_READWRITE will be set.</span></span> 
  
<span data-ttu-id="6a0c4-135">�v���p�e�B�͂��Ȃ��ύX�܂��͍폜�AIPROP_READONLY �܂��� IPROP_READWRITE �̃t���O���ݒ肳��܂��B</span><span class="sxs-lookup"><span data-stu-id="6a0c4-135">If a property has not been modified or deleted, only the IPROP_READONLY or IPROP_READWRITE flag will be set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a0c4-136">�֘A����</span><span class="sxs-lookup"><span data-stu-id="6a0c4-136">See also</span></span>



[<span data-ttu-id="6a0c4-137">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="6a0c4-137">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="6a0c4-138">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6a0c4-138">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

