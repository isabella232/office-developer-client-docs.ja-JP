---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4e478c9e8978125a37691ee5bd97fa9f1cbce077
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425156"
---
# <a name="ipropdatahrsetobjaccess"></a><span data-ttu-id="d1f9b-103">IPropData::HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="d1f9b-103">IPropData::HrSetObjAccess</span></span>

  
  
<span data-ttu-id="d1f9b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1f9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1f9b-105">�I�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="d1f9b-105">Sets the access level for the object.</span></span>
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="d1f9b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d1f9b-106">Parameters</span></span>

 <span data-ttu-id="d1f9b-107">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="d1f9b-107">_ulAccess_</span></span>
  
> <span data-ttu-id="d1f9b-p101">[����]�I�u�W�F�N�g�̃A�N�Z�X ���x����w�肷��t���O�̃r�b�g�}�b�v���܂��B�t���O����̂����ꂩ��ݒ肷�邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="d1f9b-p101">[in] A bitmask of flags that specifies the object's access level. One of the following flags can be set:</span></span>
    
<span data-ttu-id="d1f9b-110">IPROP_READONLY</span><span class="sxs-lookup"><span data-stu-id="d1f9b-110">IPROP_READONLY</span></span> 
  
> <span data-ttu-id="d1f9b-111">�ǂݎ���p�ɃI�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="d1f9b-111">Sets the object's access level to read-only.</span></span> 
    
<span data-ttu-id="d1f9b-112">IPROP_READWRITE</span><span class="sxs-lookup"><span data-stu-id="d1f9b-112">IPROP_READWRITE</span></span> 
  
> <span data-ttu-id="d1f9b-113">�I�u�W�F�N�g�̓ǂݎ��/�������݃A�N�Z�X ���x����ݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="d1f9b-113">Sets the object's access level to read/write.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d1f9b-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="d1f9b-114">Return value</span></span>

<span data-ttu-id="d1f9b-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1f9b-115">S_OK</span></span> 
  
> <span data-ttu-id="d1f9b-116">�I�u�W�F�N�g�̃A�N�Z�X ���x��������ɐݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="d1f9b-116">The object's access level was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1f9b-117">注釈</span><span class="sxs-lookup"><span data-stu-id="d1f9b-117">Remarks</span></span>

<span data-ttu-id="d1f9b-p102">**IPropData::HrSetObjAccess**���\�b�h�́A�X �̃v���p�e�B�ł͂Ȃ��A�I�u�W�F�N�g�S�̂̃A�N�Z�X ���x����ݒ肵�܂��B�I�u�W�F�N�g���쐬���ꂽ�Ƃ��Ɋm���A�N�Z�X ���x����ύX����̂ɂ́A **HrSetObjAccess**��g�p�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="d1f9b-p102">The **IPropData::HrSetObjAccess** method sets the access level for an entire object, rather than for individual properties. **HrSetObjAccess** can be used to change the access level established when the object was created.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d1f9b-120">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d1f9b-120">Notes to callers</span></span>

<span data-ttu-id="d1f9b-p103">To set an access level on a property, first call **HrSetObjAccess** with the IPROP_READWRITE flag set in the  _ulAccess_ parameter to make the object modifiable. Then call the [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) method, specifying the target property in the array pointed to by the  _lpPropTagArray_ parameter.</span><span class="sxs-lookup"><span data-stu-id="d1f9b-p103">To set an access level on a property, first call **HrSetObjAccess** with the IPROP_READWRITE flag set in the  _ulAccess_ parameter to make the object modifiable. Then call the [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) method, specifying the target property in the array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="d1f9b-123">�N���C�A���g�ɓǂݎ���p�ɂȂ�v���p�e�B��g�p���ăI�u�W�F�N�g��쐬����ɂ́A[�ǂݎ��/�������݃I�u�W�F�N�g��쐬�A�K�v�ȃv���p�e�B��ǉ��A **HrSetObjAccess**�͓ǂݎ���p�̃A�N�Z�X��ύX����̂ɂ́A[�Ăяo������܂��B</span><span class="sxs-lookup"><span data-stu-id="d1f9b-123">To create an object with properties that will be read-only to clients, create a read/write object, add the necessary properties, and then call **HrSetObjAccess** to change the object's access to read-only.</span></span> 
  
<span data-ttu-id="d1f9b-124">�N���C�A���g���V�����v���p�e�B��쐬���邱�Ƃ�h�~����̂� **HrSetObjAccess**��g�p���邱�Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="d1f9b-124">You can also use **HrSetObjAccess** to prevent clients from creating new properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1f9b-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1f9b-125">See also</span></span>



[<span data-ttu-id="d1f9b-126">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="d1f9b-126">IPropData::HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md)
  
[<span data-ttu-id="d1f9b-127">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="d1f9b-127">IPropData::HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md)
  
[<span data-ttu-id="d1f9b-128">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d1f9b-128">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

