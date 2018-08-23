---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ff088dc5bf62f407692c9eec649ff388f79d549d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567154"
---
# <a name="contabentryid"></a><span data-ttu-id="0ab3f-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0ab3f-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="0ab3f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ab3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ab3f-105">連絡先フォルダーのエントリ ID が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ab3f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0ab3f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0ab3f-107">msomapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0ab3f-107">msomapiutil.h</span></span>  <br/> |
   
```cpp
#pragma pack(4) 
typedef struct _contab_entryid
{
    BYTE abFlags[4];
    MAPIUID muid;
    ULONG ulVersion;
    ULONG ulType;
    ULONG ulIndex;
    ULONG cbeid;
    BYTE abeid[1];
}   CONTAB_ENTRYID, *LPCONTAB_ENTRYID;
#pragma pack() 
```

## <a name="members"></a><span data-ttu-id="0ab3f-108">Members</span><span class="sxs-lookup"><span data-stu-id="0ab3f-108">Members</span></span>

 <span data-ttu-id="0ab3f-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="0ab3f-109">**abFlags**</span></span>
  
> <span data-ttu-id="0ab3f-110">オブジェクトを記述する情報を提供するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="0ab3f-111">詳細については、[エントリ ID](entryid.md)の構造体の**abFlags**フィールドの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="0ab3f-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="0ab3f-112">**muid**</span></span>
  
> <span data-ttu-id="0ab3f-113">ストア プロバイダーを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="0ab3f-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="0ab3f-114">**ulVersion**</span></span>
  
> <span data-ttu-id="0ab3f-115">**CONTAB_ENTRYID**構造体のバージョン番号です。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="0ab3f-116">CONTAB_VERSION に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="0ab3f-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="0ab3f-117">**ulType**</span></span>
  
> <span data-ttu-id="0ab3f-118">連絡先のエントリ ID の種類を表す整数。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="0ab3f-119">次の値のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="0ab3f-120">**名前**</span><span class="sxs-lookup"><span data-stu-id="0ab3f-120">**Name**</span></span>|<span data-ttu-id="0ab3f-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="0ab3f-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ab3f-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="0ab3f-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="0ab3f-123">���b�Z�[�W���O ���[�U�[ �I�u�W�F�N�g�ł��B</span><span class="sxs-lookup"><span data-stu-id="0ab3f-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="0ab3f-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="0ab3f-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="0ab3f-125">�z�z���X�g �I�u�W�F�N�g�ł��B</span><span class="sxs-lookup"><span data-stu-id="0ab3f-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="0ab3f-126">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="0ab3f-126">**ulIndex**</span></span>
  
> <span data-ttu-id="0ab3f-127">電子メールのプロパティのサブセットへのインデックスです。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="0ab3f-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="0ab3f-128">**cbeid**</span></span>
  
> <span data-ttu-id="0ab3f-129">連絡先アドレス帳内のこのエントリに関連付けられている取引先担当者のメッセージのエントリ id のサイズです。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="0ab3f-130">**abeid**</span><span class="sxs-lookup"><span data-stu-id="0ab3f-130">**abeid**</span></span>
  
> <span data-ttu-id="0ab3f-131">連絡先アドレス帳内のこのエントリに関連付けられている取引先担当者のメッセージのエントリ id です。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ab3f-132">注釈</span><span class="sxs-lookup"><span data-stu-id="0ab3f-132">Remarks</span></span>

<span data-ttu-id="0ab3f-133">連絡先のアドレス帳は、アドレス帳を電子メール アドレスまたは fax 番号のいずれかを持つ連絡先フォルダー内のすべての連絡先アイテムを含むです。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="0ab3f-134">連絡先のアドレス帳内の各エントリは、電子メール アドレスまたは fax 番号のいずれかに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="0ab3f-135">連絡先アイテムは、最大 3 つの電子メール アドレスを持つことができますので、3 つの fax 番号を 6 つまでのエントリに対応する連絡先のアドレス帳で連絡先アイテムを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="0ab3f-136">連絡先のアドレス帳の目的は、ユーザーの連絡先フォルダーの連絡先に電子メール メッセージのアドレス指定をサポートします。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="0ab3f-137">Contab32.dll を Microsoft Outlook 2010 と Microsoft Outlook 2013 でサポートされる連絡先のアドレス帳プロバイダーには。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="0ab3f-138">**CONTAB_ENTRYID**構造体は、基になる MAPI 連絡先メッセージに表示される情報のサブセットをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="0ab3f-139">特定の連絡先のアドレス帳エントリが関連付けられている取引先担当者のメッセージを識別します。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="0ab3f-140">**Cbeid**と**abeid**フィールドは、 **ulType**フィールドの値は、CONTAB_DISTLIST または CONTAB_USER に設定されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="0ab3f-141">**UlType**フィールドの値を設定するには CONTAB_ROOT、CONTAB_SUBROOT、または CONTAB_CONTAINER、 [DIR_ENTRYID](dir_entryid.md)構造体を代わりに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ab3f-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0ab3f-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ab3f-142">See also</span></span>



[<span data-ttu-id="0ab3f-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0ab3f-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="0ab3f-144">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0ab3f-144">MAPI Structures</span></span>](mapi-structures.md)

