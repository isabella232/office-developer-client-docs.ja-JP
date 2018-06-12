---
title: IPropDataHrSetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetPropAccess
api_type:
- COM
ms.assetid: 02365050-5e8b-437c-925f-4eb0df646356
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 39dbf3d3c8a8e22a7b7087929f749589cdeb2090
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801173"
---
# <a name="ipropdatahrsetpropaccess"></a><span data-ttu-id="27eca-103">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="27eca-103">IPropData::HrSetPropAccess</span></span>

  
  
<span data-ttu-id="27eca-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27eca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27eca-105">�A�N�Z�X ���x���܂��̓I�u�W�F�N�g�̃v���p�e�B�� 1 �ȏ�̏�Ԃ�ݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="27eca-105">Sets the access level or status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="27eca-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="27eca-106">Parameters</span></span>

 <span data-ttu-id="27eca-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="27eca-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="27eca-108">[����]�v���p�e�B��ύX�ł��邱�Ƃ�����v���p�e�B �^�O�̔z��ւ̃|�C���^�[�B</span><span class="sxs-lookup"><span data-stu-id="27eca-108">[in] A pointer to an array of property tags that indicate the properties to be modified.</span></span> 
    
 <span data-ttu-id="27eca-109">_rgulAccess_</span><span class="sxs-lookup"><span data-stu-id="27eca-109">_rgulAccess_</span></span>
  
> <span data-ttu-id="27eca-p101">[����]�t���O �r�b�g�}�X�N�̔z�񂵂܂��B�e�r�b�g�́A�A�N�Z�X ���x���̏��]�A�܂��͂��̗����� _lpPropTagArray_�p�����[�^�[���Q�ƁA�z���̓���̃v���p�e�B�̊e���\������܂��B2 �̔z��A�ʒu _rgulAccess_�ōŏ��̃r�b�g�ɂ��Đ���ŏ��̃v���p�e�B�� _lpPropTagArray_�|�C���g�ɁA���̂ł��B �v���p�e�B�̃^�O���ƂɁA1 �̃A�N�Z�X ���x���̃t���O�� 1 �̃t���O��ݒ�ł��܂��B���̕\�́A�\�ȃt���O������܂��B</span><span class="sxs-lookup"><span data-stu-id="27eca-p101">[in] An array of flag bitmasks. Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array that the  _lpPropTagArray_ parameter points to. The two arrays are positional in that the first bitmask in  _rgulAccess_ describes the first property that  _lpPropTagArray_ points to, and so on. For each property tag, one access-level flag and one status flag can be set. The following table shows the possible flags.</span></span> 
    
|<span data-ttu-id="27eca-115">**�A�N�Z�X ���x���̃t���O**</span><span class="sxs-lookup"><span data-stu-id="27eca-115">**Access-level flag**</span></span>|<span data-ttu-id="27eca-116">**�t���O�̏��**</span><span class="sxs-lookup"><span data-stu-id="27eca-116">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="27eca-117">�v���p�e�B��ύX�ł��Ȃ����Ƃ�����AIPROP_READONLY</span><span class="sxs-lookup"><span data-stu-id="27eca-117">IPROP_READONLY, which indicates that the property cannot be modified</span></span>  <br/> |<span data-ttu-id="27eca-118">IPROP_CLEAN �v���p�e�B���ύX����Ă��Ȃ����Ƃ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="27eca-118">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="27eca-119">IPROP_READWRITE �v���p�e�B��ύX�ł��邱�Ƃ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="27eca-119">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="27eca-120">IPROP_DIRTY �v���p�e�B���ύX����Ă��邱�Ƃ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="27eca-120">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="27eca-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="27eca-121">Return value</span></span>

<span data-ttu-id="27eca-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="27eca-122">S_OK</span></span> 
  
> <span data-ttu-id="27eca-123">�A�N�Z�X ���x���Ə�Ԃ̃t���O������ɐݒ肳��Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="27eca-123">The access-level and status flags have been successfully set.</span></span>
    
<span data-ttu-id="27eca-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="27eca-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="27eca-125">�ǂݎ���p�I�u�W�F�N�g�܂��͔��M�҂��\���ȃA�N�Z�X��������Ă���I�u�W�F�N�g�̃v���p�e�B��ݒ肵�܂����B</span><span class="sxs-lookup"><span data-stu-id="27eca-125">An attempt was made to set a property on a read-only object or an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="27eca-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="27eca-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="27eca-127">_rgulAccess_�p�����[�^�[�ɂ́A�t���O�AIPROP_READONLY IPROP_READWRITE �Ȃǂ̖����ȑg�ݍ��킹���܂܂�Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="27eca-127">The  _rgulAccess_ parameter contains an invalid combination of flags, such as IPROP_READONLY and IPROP_READWRITE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="27eca-128">����</span><span class="sxs-lookup"><span data-stu-id="27eca-128">Remarks</span></span>

<span data-ttu-id="27eca-p102">**IPropData::HrSetPropAccess**���\�b�h�́A�A�N�Z�X ���x������� [lpPropTagArray](sproptagarray.md)�p�����[�^�[��w��_SPropTagArray_�\���̃v���p�e�B �^�O�Ŏ��ʂ����v���p�e�B�̏�Ԃ�ύX���܂��B�e�v���p�e�B�ɂ� _rgulAccess_�z��őΉ�����G���g��������܂��B1 �̃t���O������v���p�e�B�̃A�N�Z�X ���x���ʂɁA�Y������G���g����ݒ�ł��܂���Ԃ�����t���O��ݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="27eca-p102">The **IPropData::HrSetPropAccess** method changes the access level and status for the properties that are identified by the property tags in the [SPropTagArray](sproptagarray.md) structure pointed to by the  _lpPropTagArray_ parameter. For each property, there is a corresponding entry in the  _rgulAccess_ array. The entry can be set to one flag that indicates the property's access level and another flag that indicates its status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="27eca-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="27eca-132">Notes to callers</span></span>

<span data-ttu-id="27eca-133">����̃v���p�e�B] �̒l���ύX���ꂽ�Ƃ��Ɍ��肵����A�I�u�W�F�N�g�̃v���p�e�B�� 1 �ȏ�̃A�N�Z�X ���x����ύX����̂ɂ́A **HrSetPropAccess**��g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="27eca-133">Use **HrSetPropAccess** to determine when a particular property value changes and to change the access level for one or more of an object's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="27eca-134">�֘A����</span><span class="sxs-lookup"><span data-stu-id="27eca-134">See also</span></span>



[<span data-ttu-id="27eca-135">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="27eca-135">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="27eca-136">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="27eca-136">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

