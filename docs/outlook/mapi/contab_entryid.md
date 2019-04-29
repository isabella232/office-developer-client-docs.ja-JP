---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a2a204f76b62c8c6bc6d8a4e793c936a0184dc65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424085"
---
# <a name="contabentryid"></a><span data-ttu-id="85c9a-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="85c9a-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="85c9a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85c9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85c9a-105">連絡先フォルダーのエントリ ID を格納します。</span><span class="sxs-lookup"><span data-stu-id="85c9a-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="85c9a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="85c9a-106">Header file:</span></span>  <br/> |<span data-ttu-id="85c9a-107">msomapiutil</span><span class="sxs-lookup"><span data-stu-id="85c9a-107">msomapiutil.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="85c9a-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="85c9a-108">Members</span></span>

 <span data-ttu-id="85c9a-109">**abflags**</span><span class="sxs-lookup"><span data-stu-id="85c9a-109">**abFlags**</span></span>
  
> <span data-ttu-id="85c9a-110">オブジェクトについての情報を提供するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="85c9a-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="85c9a-111">詳細については、 [ENTRYID](entryid.md)構造の**abflags**フィールドの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85c9a-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="85c9a-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="85c9a-112">**muid**</span></span>
  
> <span data-ttu-id="85c9a-113">ストアプロバイダーを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="85c9a-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="85c9a-114">**ulversion**</span><span class="sxs-lookup"><span data-stu-id="85c9a-114">**ulVersion**</span></span>
  
> <span data-ttu-id="85c9a-115">**CONTAB_ENTRYID**構造体のバージョン番号。</span><span class="sxs-lookup"><span data-stu-id="85c9a-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="85c9a-116">CONTAB_VERSION に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85c9a-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="85c9a-117">**ultype**</span><span class="sxs-lookup"><span data-stu-id="85c9a-117">**ulType**</span></span>
  
> <span data-ttu-id="85c9a-118">連絡先エントリ ID の種類を表す整数。</span><span class="sxs-lookup"><span data-stu-id="85c9a-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="85c9a-119">次のいずれかの値であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="85c9a-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="85c9a-120">**名前**</span><span class="sxs-lookup"><span data-stu-id="85c9a-120">**Name**</span></span>|<span data-ttu-id="85c9a-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="85c9a-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85c9a-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="85c9a-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="85c9a-123">メッセージングを処理するユーザー オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="85c9a-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="85c9a-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="85c9a-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="85c9a-125">�z�z���X�g �I�u�W�F�N�g�ł��B</span><span class="sxs-lookup"><span data-stu-id="85c9a-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="85c9a-126">**ulindex**</span><span class="sxs-lookup"><span data-stu-id="85c9a-126">**ulIndex**</span></span>
  
> <span data-ttu-id="85c9a-127">電子メールプロパティのサブセットに対するインデックス。</span><span class="sxs-lookup"><span data-stu-id="85c9a-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="85c9a-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="85c9a-128">**cbeid**</span></span>
  
> <span data-ttu-id="85c9a-129">連絡先のアドレス帳で、このエントリに関連付けられている連絡先メッセージのエントリ id のサイズ。</span><span class="sxs-lookup"><span data-stu-id="85c9a-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="85c9a-130">**abeid**</span><span class="sxs-lookup"><span data-stu-id="85c9a-130">**abeid**</span></span>
  
> <span data-ttu-id="85c9a-131">連絡先アドレス帳のこのエントリに関連付けられている連絡先メッセージのエントリ識別子。</span><span class="sxs-lookup"><span data-stu-id="85c9a-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85c9a-132">注釈</span><span class="sxs-lookup"><span data-stu-id="85c9a-132">Remarks</span></span>

<span data-ttu-id="85c9a-133">連絡先アドレス帳は、電子メールアドレスまたは fax 番号のいずれかの連絡先フォルダー内のすべての連絡先アイテムを含むアドレス帳です。</span><span class="sxs-lookup"><span data-stu-id="85c9a-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="85c9a-134">連絡先のアドレス帳の各エントリは、電子メールアドレスまたは fax 番号と関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="85c9a-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="85c9a-135">連絡先アイテムは最大3つの電子メールアドレスと3つの fax 番号を持つことができるので、連絡先アイテムは対応する連絡先アドレス帳の最大6つのエントリで表すことができます。</span><span class="sxs-lookup"><span data-stu-id="85c9a-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="85c9a-136">連絡先アドレス帳の目的は、連絡先フォルダー内の連絡先に電子メールメッセージを送信するユーザーをサポートすることです。</span><span class="sxs-lookup"><span data-stu-id="85c9a-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="85c9a-137">microsoft outlook 2010 および microsoft outlook 2013 がサポートしている連絡先アドレス帳プロバイダーは contab32 です。</span><span class="sxs-lookup"><span data-stu-id="85c9a-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="85c9a-138">**CONTAB_ENTRYID**構造体は、基になる MAPI 連絡先メッセージ内に存在する情報のサブセットをサポートします。</span><span class="sxs-lookup"><span data-stu-id="85c9a-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="85c9a-139">特定の連絡先アドレス帳エントリに関連付けられている連絡先メッセージを識別します。</span><span class="sxs-lookup"><span data-stu-id="85c9a-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="85c9a-140">**cbeid**および**abeid**フィールドは、 **ultype**フィールドの値が CONTAB_DISTLIST または CONTAB_USER に設定されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="85c9a-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="85c9a-141">**ultype**フィールドの値が CONTAB_ROOT、CONTAB_SUBROOT、または CONTAB_CONTAINER に設定されている場合は、代わりに[DIR_ENTRYID](dir_entryid.md)構造を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85c9a-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85c9a-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="85c9a-142">See also</span></span>



[<span data-ttu-id="85c9a-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="85c9a-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="85c9a-144">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="85c9a-144">MAPI Structures</span></span>](mapi-structures.md)

