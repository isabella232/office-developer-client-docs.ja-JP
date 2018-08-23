---
title: IMessageModifyRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.ModifyRecipients
api_type:
- COM
ms.assetid: 2625f29d-325f-417d-bcec-49d580f9cd7e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0735008575db5e1cab62dbde4b699b15e04cedb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567287"
---
# <a name="imessagemodifyrecipients"></a><span data-ttu-id="a3f8d-103">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="a3f8d-103">IMessage::ModifyRecipients</span></span>

  
  
<span data-ttu-id="a3f8d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3f8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3f8d-105">�ǉ��A�폜�A�܂��̓��b�Z�[�W�̎�M�҂�ύX���܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-105">Adds, deletes, or modifies message recipients.</span></span>
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a><span data-ttu-id="a3f8d-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="a3f8d-106">Parameters</span></span>

 <span data-ttu-id="a3f8d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a3f8d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a3f8d-p101">[����]��M�҂̕ύX�𐧌䂷��t���O�̃r�b�g���܂��B _ulFlags_�p�����[�^�[�̃[����o�߂���ƁA **ModifyRecipients**�� _lpMods_�p�����[�^�[�Ŏw�肳�ꂽ����̃��X�g�Ŋ����̂��ׂĂ̎�M�҂�u�������܂��B _ulFlags_�ɂ́A���̃t���O��ݒ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-p101">[in] Bitmask of flags that controls the recipient changes. If zero is passed for the  _ulFlags_ parameter, **ModifyRecipients** replaces all existing recipients with the recipient list pointed to by the  _lpMods_ parameter. The following flags can be set for  _ulFlags_:</span></span>
    
<span data-ttu-id="a3f8d-111">MODRECIP_ADD</span><span class="sxs-lookup"><span data-stu-id="a3f8d-111">MODRECIP_ADD</span></span> 
  
> <span data-ttu-id="a3f8d-112">_lpMods_�p�����[�^�[��w����M�҂́A����̃��X�g�ɒǉ�����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-112">The recipients pointed to by the  _lpMods_ parameter should be added to the recipient list.</span></span> 
    
<span data-ttu-id="a3f8d-113">MODRECIP_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a3f8d-113">MODRECIP_MODIFY</span></span> 
  
> <span data-ttu-id="a3f8d-p102">_lpMods_�p�����[�^�[��w����M�҂́A�����̎�M�҂ɒu�������Ă��������B���ׂĂ̊����̃v���p�e�B�́A�Ή�����[ADRENTRY](adrentry.md)�\����ɒu���������܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-p102">The recipients pointed to by the  _lpMods_ parameter should replace existing recipients. All of the existing properties are replaced by those in the corresponding [ADRENTRY](adrentry.md) structure.</span></span> 
    
<span data-ttu-id="a3f8d-116">MODRECIP_REMOVE</span><span class="sxs-lookup"><span data-stu-id="a3f8d-116">MODRECIP_REMOVE</span></span> 
  
> <span data-ttu-id="a3f8d-117">インデックスとして、 _lpMods_パラメーターの各受信者のエントリのプロパティの値の配列に含まれる**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) プロパティを使用して受信者の一覧から既存の受信者を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3f8d-117">Existing recipients should be removed from the recipient list using as an index the **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) property included in the property value array of each recipient entry in the  _lpMods_ parameter.</span></span> 
    
 <span data-ttu-id="a3f8d-118">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="a3f8d-118">_lpMods_</span></span>
  
> <span data-ttu-id="a3f8d-119">[����]�|�C���^�[��ǉ��A�폜�A�܂��̓��b�Z�[�W��ɕύX���ꂽ����̃��X�g��܂�[ADRLIST](adrlist.md)�\���ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-119">[in] Pointer to an [ADRLIST](adrlist.md) structure that contains a list of recipients to be added, deleted, or modified in the message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a3f8d-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a3f8d-120">Return value</span></span>

<span data-ttu-id="a3f8d-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3f8d-121">S_OK</span></span> 
  
> <span data-ttu-id="a3f8d-122">���惊�X�g������ɕύX����܂����B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-122">The recipient list was successfully modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3f8d-123">����</span><span class="sxs-lookup"><span data-stu-id="a3f8d-123">Remarks</span></span>

<span data-ttu-id="a3f8d-p103">**IMessage::ModifyRecipients**���\�b�h�́A���b�Z�[�W�̎�M�҃��X�g��ύX���܂��B���̃��X�g����A��M�҂̃e�[�u�����g�ݍ��܂�Ă���A [ADRLIST](adrlist.md)�\����ɕێ��͂ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-p103">The **IMessage::ModifyRecipients** method changes the message's recipient list. It is from this list, held in an [ADRLIST](adrlist.md) structure, that the recipient table is built.</span></span> 
  
<span data-ttu-id="a3f8d-126">**ADRLIST**�\���̊e��M�҂� 1 ��[ADRENTRY](adrentry.md)�\�����܂܂�Ă��邵�A�e **ADRENTRY**�\���ɂ́A��M�҂̃v���p�e�B��L�q����v���p�e�B�̒l�̔z�񂪊܂܂�Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-126">The **ADRLIST** structure contains one [ADRENTRY](adrentry.md) structure for each recipient and each **ADRENTRY** structure contains an array of property values describing the recipient properties.</span></span> 
  
<span data-ttu-id="a3f8d-127">**ADRLIST**構造内の受信者を解決または未解決のことができます。</span><span class="sxs-lookup"><span data-stu-id="a3f8d-127">Recipients in the **ADRLIST** structure can be resolved or unresolved.</span></span> <span data-ttu-id="a3f8d-128">数と含まれているプロパティの種類が異なります。</span><span class="sxs-lookup"><span data-stu-id="a3f8d-128">The difference is in the number and type of properties that are included.</span></span> <span data-ttu-id="a3f8d-129">未解決の受信者が含まれ**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) と**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティのみ、解決済みの受信者には、これら 2 つのプロパティに加え、 **PR_ADDRTYPE が含まれています。**([PidTagAddressType](pidtagaddresstype-canonical-property.md)) と**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="a3f8d-129">An unresolved recipient contains only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) properties while a resolved recipient contains those two properties plus **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span> <span data-ttu-id="a3f8d-130">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) が利用可能な場合は、ことができます含まれてもします。</span><span class="sxs-lookup"><span data-stu-id="a3f8d-130">If **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is available, it can be included also.</span></span>
  
<span data-ttu-id="a3f8d-p105">���b�Z�[�W�����M�����܂łɂ́A���̎�M�҈ꗗ�ŉ����M�҂݂̂ɕK�v������܂��B��M�҂ɂ́A�z�M�s�\���|�[�g��쐬���A���̃��b�Z�[�W�̑��M�҂ɑ��M���ꂽ���������܂��B�N���C�A���g�̊ϓ[���疼�O����v���Z�X�̏ڍׂɂ��ẮA[���O��������](resolving-a-recipient-name.md)��Q�Ƃ��Ă��������B�A�h���X���̃v���o�C�](resolving-a-recipient-name.md)�[�̊ϓ_����̏ڍׂɂ��ẮA[���O������������](implementing-name-resolution.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-p105">By the time a message is submitted, it must include only resolved recipients in its recipient list. Unresolved recipients cause nondelivery reports to be created and sent to the original sender of the message. For more information about the name resolution process from the client perspective, see [Resolving a Name](resolving-a-recipient-name.md). For more information from the perspective of the address book provider, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="a3f8d-p106">�ɉ����ĉ������і�����̎�M�҂��M�҂� NULL ���Ƃ��ł��܂��B��M�҂� **ADRENTRY**�\���� **cValues**�����o�[�� 0 �ɐݒ肵�A **rgPropVals**�����o�[�� NULL �ɐݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-p106">In addition to resolved and unresolved recipients, a recipient can be NULL. The **cValues** member of the **ADRENTRY** structure for the recipient is set to zero and the **rgPropVals** member is set to NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a3f8d-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a3f8d-137">Notes to callers</span></span>

<span data-ttu-id="a3f8d-138">コモン ダイアログ ボックスを表示し、エントリを選択するように求めるには、 [IAddrBook::Address](imapisupport-address.md)を呼び出すことによって、受信者のリストを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a3f8d-138">You can create a recipient list by calling [IAddrBook::Address](imapisupport-address.md) to display the common dialog box and prompt the user to select entries.</span></span> <span data-ttu-id="a3f8d-139">**アドレス**に_lppAdrList_パラメーターで指定されたアドレス一覧は、 **ModifyRecipients**に_lpMods_のパラメーターとして渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="a3f8d-139">The address list pointed to by the  _lppAdrList_ parameter to **Address** can be passed to **ModifyRecipients** as the  _lpMods_ parameter.</span></span> 
  
<span data-ttu-id="a3f8d-p108">[ADRLIST](adrlist.md)�\����Ŏ�M�҂̃v���p�e�B��w�肷��ꍇ�́A���ׂĂ̒ǉ��܂��͕ύX���ꂽ��̂����łȂ��A��M�҂̃v���p�e�B��w�肵�܂��B��M�҂��ύX���ꂽ�Ƃ� **ADRLIST**�\���Ɋ܂܂�Ă��Ȃ��C�ӂ̃v���p�e�B���폜����܂��B���݂̈�A�̃v���p�e�B�̂��ׂẴ��b�Z�[�W�̎�M�҂�擾����ɂ͂���ɂ́A [GetRecipientTable](imessage-getrecipienttable.md)����ׂĂ̍s��擾���܂��B **SRowSet**�ɂ́A **ADRLIST**�\����Ɠ����ł��邽�ߓ����Ӗ��Ŏg�p�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-p108">When you specify properties for a recipient in the [ADRLIST](adrlist.md) structure, include all of the recipient's properties, not only the new or changed ones. When a recipient is modified, any properties not included in the **ADRLIST** structure are deleted. To retrieve the current set of properties for all of a message's recipients, call [GetRecipientTable](imessage-getrecipienttable.md) and retrieve all of the rows. Because an **SRowSet** is identical in structure to an **ADRLIST**, you can use them interchangeably.</span></span>
  
 <span data-ttu-id="a3f8d-144">**ModifyRecipients**�ɂ́A  _ulFlags_�p�����[�^�[�Ȃ��̃t���O�̐ݒ肳��Ă���ꍇ�A  _lpMods_���w������܂ނ��ׂĂ̌��݂̎�M�҃��X�g�̃G���g�����u���������܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-144">**ModifyRecipients** replaces all of the entries in the current recipient list with the information pointed to by  _lpMods_ when none of the flags are set in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a3f8d-145">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a3f8d-145">Notes to callers</span></span>

<span data-ttu-id="a3f8d-p109">MODRECIP_MODIFY �t���O��ݒ肷��Ƃ��� **ModifyRecipients** [lpMods](adrlist.md)�ɓn�����_ADRLIST_�\���Ɋ֘A�t�����Ă���s�S�̂̎�M�Ҋe�s�ɒu�������܂��B���ׂĂ̎�M�҂��Ӑ}�����ɍ폜����Ȃ��悤�ɕύX����Ă��邩�ǂ����Ɋ֌W�Ȃ��A�v���p�e�B��w�肷��悤�ɒ��ӂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-p109">When you set the MODRECIP_MODIFY flag, **ModifyRecipients** replaces each entire recipient row with the associated row in the [ADRLIST](adrlist.md) structure passed in  _lpMods_. Be careful to specify all of the properties that a recipient should have regardless of whether they have changed to prevent them from being unintentionally deleted.</span></span>
  
<span data-ttu-id="a3f8d-148">�ȉ��́A **ADRLIST**�\���Ŏ�M�҂̃v���p�e�B��ݒ肷�邽�߂̂������̃��[���ł��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-148">Following are some rules for setting the properties of the recipients in the **ADRLIST** structure:</span></span> 
  
- <span data-ttu-id="a3f8d-p110">�v���p�e�B�̌^�Ƃ��� PT_NULL ��g��Ȃ��ł��������B **ModifyRecipients** �ł́A���̒l�����������ꍇ�A�G���[���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-p110">Do not use PT_NULL as a property type. **ModifyRecipients** returns an error when encountering this value.</span></span> 
    
- <span data-ttu-id="a3f8d-p111">�v���p�e�B�̌^�Ƃ��� PT_ERROR ��g��Ȃ��ł��������B **ModifyRecipients** �ł́A���̒l�͖������܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-p111">Do not use PT_ERROR as a property type. **ModifyRecipients** ignores this value.</span></span> 
    
- <span data-ttu-id="a3f8d-153">**ulFlags**�� MODRECIP_REMOVE �܂��� MODRECIP_MODIFY �̂����ꂩ�̃t���O��ݒ肷��ƁA���ׂĂ̎�M�҂ɑ΂��āA _PR_ROWID_�v���p�e�B���܂܂�܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-153">Include the **PR_ROWID** property for all recipients when you set either the MODRECIP_REMOVE or MODRECIP_MODIFY flag in  _ulFlags_.</span></span> 
    
- <span data-ttu-id="a3f8d-154">**ulFlags**�܂��� _ulFlags_�Ƀ[����ʉ߂���Ƃ��ɁAMODRECIP_ADD �t���O��ݒ肷��Ƃ��ɁA��M�҂̂����ꂩ�� _PR_ROWID_�v���p�e�B��܂߂Ȃ��ł��������B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-154">Do not include the **PR_ROWID** property for any of the recipients when you set the MODRECIP_ADD flag in  _ulFlags_ or when you pass zero in  _ulFlags_.</span></span>
    
<span data-ttu-id="a3f8d-p112">��M�҂� 1 �� **PR_ADDRTYPE**�v���p�e�B�܂��� **PR_EMAIL_ADDRESS**�v���p�e�B��ǉ�����A�܂��͗����̃v���p�e�B�� **PR_ENTRYID**�Ŏ������悤�ɁA��M�҂̃A�h���X�A�Z���̎�ނƈ�v���Ȃ��A���ʂ͒�\`����Ă��܂���B�܂�A�T�[�r�X �v���o�C�_�[�ɂ���ẮA���� 3 �̉\��������܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-p112">If you include either the **PR_ADDRTYPE** property or **PR_EMAIL_ADDRESS** property for a recipient and one or both of these properties are inconsistent with the address type and address of the recipient as identified by **PR_ENTRYID**, the results are undefined. That is, there are three possibilities, depending on the service provider:</span></span>
  
- <span data-ttu-id="a3f8d-157">���b�Z�[�W�́A **PR_ADDRTYPE**�� **PR_EMAIL_ADDRESS**�v���p�e�B�Ő������Ă���A�h���X�ɔz�M����܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-157">The message will be delivered to the address described by the **PR_ADDRTYPE** and **PR_EMAIL_ADDRESS** properties.</span></span> 
    
- <span data-ttu-id="a3f8d-158">**PR_ENTRYID**�Ŏ����ꂽ��M�҂Ƀ��b�Z�[�W���z�M����܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-158">The message will be delivered to the recipient identified by **PR_ENTRYID**.</span></span>
    
- <span data-ttu-id="a3f8d-159">���b�Z�[�W�́A�Z���̂����܂����������Ŕz�M�s�\�錾����܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-159">The message will be declared undeliverable due to the ambiguity of the address information.</span></span>
    
<span data-ttu-id="a3f8d-p113">���惊�X�g�̃��������蓖��[ADRLIST �� SRowSet �\���̃�������Ǘ�����](managing-memory-for-adrlist-and-srowset-structures.md)�Ő�����Ă��銄�蓖�ă��[����g�p���܂��B **ADRLIST**�\����̃T�u�\���̂����ꂩ�� **ModifyRecipients**�������܂���B **ADRLIST**�\���Ɗe[SPropValue](spropvalue.md)�\���̂́A���ꂼ��ʂɉ�����邱�Ƃ��ł��܂����A [MAPIAllocateBuffer](mapiallocatebuffer.md)�֐���g�p���ČʂɊ��蓖�Ă���K�v������܂��B���@�ł́A�C�ӂ� **SPropValue**�\���̒ǉ��̗̈��K�v�Ƃ���ꍇ�A���Ƃ��ł��܂� **SPropValue**�\����Œu��������V����[MAPIFreeBuffer](mapifreebuffer.md)��g�p���Č�ŉ���ł��܂��B **MAPIFreeBuffer**��g�p���Ă�A���� **SPropValue**�\����������K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-p113">Use the allocation rules outlined in [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md) to allocate memory for the recipient list. **ModifyRecipients** does not free the **ADRLIST** structure nor any of its substructures. The **ADRLIST** structure and each [SPropValue](spropvalue.md) structure must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function such that each can be freed individually. If the method requires additional space for any **SPropValue** structure, it can replace the **SPropValue** structure with a new one that can later be freed using [MAPIFreeBuffer](mapifreebuffer.md). The original **SPropValue** structure should also be freed using **MAPIFreeBuffer**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a3f8d-165">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="a3f8d-165">MFCMAPI reference</span></span>

<span data-ttu-id="a3f8d-166">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-166">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a3f8d-167">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="a3f8d-167">**File**</span></span>|<span data-ttu-id="a3f8d-168">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="a3f8d-168">**Function**</span></span>|<span data-ttu-id="a3f8d-169">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="a3f8d-169">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a3f8d-170">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a3f8d-170">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a3f8d-171">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="a3f8d-171">AddRecipient</span></span>  <br/> |<span data-ttu-id="a3f8d-172">MFCMAPI �ł́A **IMessage::ModifyRecipients**���\�b�h��g�p���āA���b�Z�[�W�ɁA�V������M�҂�ǉ����܂��B</span><span class="sxs-lookup"><span data-stu-id="a3f8d-172">MFCMAPI uses the **IMessage::ModifyRecipients** method to add a new recipient to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3f8d-173">�֘A����</span><span class="sxs-lookup"><span data-stu-id="a3f8d-173">See also</span></span>



[<span data-ttu-id="a3f8d-174">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="a3f8d-174">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="a3f8d-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="a3f8d-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="a3f8d-176">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="a3f8d-176">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="a3f8d-177">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="a3f8d-177">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="a3f8d-178">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a3f8d-178">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="a3f8d-179">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a3f8d-179">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a3f8d-180">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a3f8d-180">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="a3f8d-181">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a3f8d-181">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


<span data-ttu-id="a3f8d-182">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="a3f8d-182">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

