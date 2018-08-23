---
title: MAPI の定数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d6d6c55776c1379ec1dab0e9a6f7ef0943d2480e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801350"
---
# <a name="mapi-constants"></a><span data-ttu-id="45b2d-103">MAPI の定数</span><span class="sxs-lookup"><span data-stu-id="45b2d-103">MAPI constants</span></span>

<span data-ttu-id="45b2d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45b2d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45b2d-105">このトピックには、定数の定義、MAPI インターフェイスの宣言、および MAPI Api で使用されるクラスとインタ フェースの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-105">This topic contains constant definitions, MAPI interface declarations, and class and interface identifiers used by the MAPI APIs.</span></span>
  
## <a name="class-and-interface-identifiers"></a><span data-ttu-id="45b2d-106">クラス識別子とインターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="45b2d-106">Class and interface identifiers</span></span>

<span data-ttu-id="45b2d-107">DEFINE_GUID マクロを Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル guiddef.h に定義されているを使用して、特に明記しない限りの値は、シンボル名のグローバル一意識別子 (GUID) を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-107">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values, unless otherwise indicated.</span></span>
  
## <a name="attachment-security-conversion-api"></a><span data-ttu-id="45b2d-108">添付ファイル セキュリティの変換 API</span><span class="sxs-lookup"><span data-stu-id="45b2d-108">Attachment security conversion API</span></span>

<span data-ttu-id="45b2d-109">ここには、添付ファイル セキュリティ API の定数の定義およびインタ フェース識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-109">This section contains constant definitions and interface identifiers for the Attachment Security API.</span></span>
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

<span data-ttu-id="45b2d-110">純粋仮想関数**[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)** を定義するのにには、Windows SDK のヘッダー ファイル mapidefs.h に定義されている MAPIMETHOD マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-110">Use the MAPIMETHOD macro defined in the Windows SDK header file mapidefs.h to define the pure virtual function **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span></span> 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

<span data-ttu-id="45b2d-111">**[IAttachmentSecurity](iattachmentsecurityiunknown.md)** の仮想メソッド テーブルを定義するのにには、Windows SDK のヘッダー ファイル mapidefs.h に定義されている DECLARE_MAPI_INTERFACE_ マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-111">Use the DECLARE_MAPI_INTERFACE_ macro defined in the Windows SDK header file mapidefs.h to define the virtual method table for **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span></span> 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a><span data-ttu-id="45b2d-112">MAPI から MIME への変換 API</span><span class="sxs-lookup"><span data-stu-id="45b2d-112">MAPI-MIME conversion API</span></span>

<span data-ttu-id="45b2d-113">このセクションには、MAPI から MIME 変換 API の定数の定義、クラス識別子とインターフェイス識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-113">This section contains constant definitions and class and interface identifiers for the MAPI-MIME Conversion API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="45b2d-114">定数</span><span class="sxs-lookup"><span data-stu-id="45b2d-114">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45b2d-115">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="45b2d-115">CCSF_SMTP</span></span>  <br/> |<span data-ttu-id="45b2d-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="45b2d-116">0x0002</span></span>  <br/> |
|<span data-ttu-id="45b2d-117">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="45b2d-117">CCSF_NOHEADERS</span></span>  <br/> |<span data-ttu-id="45b2d-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="45b2d-118">0x0004</span></span>  <br/> |
|<span data-ttu-id="45b2d-119">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="45b2d-119">CCSF_USE_TNEF</span></span>  <br/> | <span data-ttu-id="45b2d-120">0x0010</span><span class="sxs-lookup"><span data-stu-id="45b2d-120">0x0010</span></span>  <br/> |
|<span data-ttu-id="45b2d-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="45b2d-121">CCSF_INCLUDE_BCC</span></span>  <br/> |<span data-ttu-id="45b2d-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="45b2d-122">0x0020</span></span>  <br/> |
|<span data-ttu-id="45b2d-123">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="45b2d-123">CCSF_8BITHEADERS</span></span>  <br/> | <span data-ttu-id="45b2d-124">0x0040</span><span class="sxs-lookup"><span data-stu-id="45b2d-124">0x0040</span></span>  <br/> |
|<span data-ttu-id="45b2d-125">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="45b2d-125">CCSF_USE_RTF</span></span>  <br/> |<span data-ttu-id="45b2d-126">0x0080</span><span class="sxs-lookup"><span data-stu-id="45b2d-126">0x0080</span></span>  <br/> |
|<span data-ttu-id="45b2d-127">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="45b2d-127">CCSF_PLAIN_TEXT_ONLY</span></span>  <br/> |<span data-ttu-id="45b2d-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="45b2d-128">0x1000</span></span>  <br/> |
|<span data-ttu-id="45b2d-129">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="45b2d-129">CCSF_NO_MSGID</span></span>  <br/> |<span data-ttu-id="45b2d-130">0x4000</span><span class="sxs-lookup"><span data-stu-id="45b2d-130">0x4000</span></span>  <br/> |
|<span data-ttu-id="45b2d-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="45b2d-131">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="45b2d-132">*Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル winerror.h で定義されています。*</span><span class="sxs-lookup"><span data-stu-id="45b2d-132">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="45b2d-133">クラス識別子</span><span class="sxs-lookup"><span data-stu-id="45b2d-133">Class identifiers</span></span>

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a><span data-ttu-id="45b2d-134">インターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="45b2d-134">Interface identifiers</span></span>

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a><span data-ttu-id="45b2d-135">オフライン状態の API</span><span class="sxs-lookup"><span data-stu-id="45b2d-135">Offline State API</span></span>

<span data-ttu-id="45b2d-136">このセクションには、オフライン状態 API の定数の定義、クラス識別子とインターフェイス識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-136">This section contains constant definitions and class and interface identifiers for the Offline State API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="45b2d-137">定数</span><span class="sxs-lookup"><span data-stu-id="45b2d-137">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45b2d-138">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="45b2d-138">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="45b2d-139">*Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル winerror.h で定義されています。*</span><span class="sxs-lookup"><span data-stu-id="45b2d-139">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="45b2d-140">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="45b2d-140">E_NOINTERFACE</span></span>  <br/> | <span data-ttu-id="45b2d-141">*Windows (SDK) のヘッダー ファイル winerror.h で定義されています。*</span><span class="sxs-lookup"><span data-stu-id="45b2d-141">*As defined in the Windows (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="45b2d-142">MAPIOFFLINE_ADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="45b2d-142">MAPIOFFLINE_ADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="45b2d-143">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="45b2d-143">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="45b2d-144">MAPIOFFLINE_UNADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="45b2d-144">MAPIOFFLINE_UNADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="45b2d-145">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="45b2d-145">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="45b2d-146">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="45b2d-146">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span></span>  <br/> |<span data-ttu-id="45b2d-147">1</span><span class="sxs-lookup"><span data-stu-id="45b2d-147">1</span></span>  <br/> |
|<span data-ttu-id="45b2d-148">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="45b2d-148">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="45b2d-149">0x1</span><span class="sxs-lookup"><span data-stu-id="45b2d-149">0x1</span></span>  <br/> |
|<span data-ttu-id="45b2d-150">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="45b2d-150">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="45b2d-151">0x2</span><span class="sxs-lookup"><span data-stu-id="45b2d-151">0x2</span></span>  <br/> |
|<span data-ttu-id="45b2d-152">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="45b2d-152">MAPIOFFLINE_FLAG_BLOCK</span></span>  <br/> |<span data-ttu-id="45b2d-153">0x00002000</span><span class="sxs-lookup"><span data-stu-id="45b2d-153">0x00002000</span></span>  <br/> |
|<span data-ttu-id="45b2d-154">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="45b2d-154">MAPIOFFLINE_FLAG_DEFAULT</span></span>  <br/> |<span data-ttu-id="45b2d-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45b2d-155">0x00000000</span></span>  <br/> |
|<span data-ttu-id="45b2d-156">MAPIOFFLINE_STATE_ALL</span><span class="sxs-lookup"><span data-stu-id="45b2d-156">MAPIOFFLINE_STATE_ALL</span></span>  <br/> |<span data-ttu-id="45b2d-157">0x003f037f</span><span class="sxs-lookup"><span data-stu-id="45b2d-157">0x003f037f</span></span>  <br/> |
|<span data-ttu-id="45b2d-158">**オンラインあるいはオフライン**</span><span class="sxs-lookup"><span data-stu-id="45b2d-158">**Online or offline**</span></span> <br/> ||
|<span data-ttu-id="45b2d-159">MAPIOFFLINE_STATE_OFFLINE_MASK</span><span class="sxs-lookup"><span data-stu-id="45b2d-159">MAPIOFFLINE_STATE_OFFLINE_MASK</span></span>  <br/> |<span data-ttu-id="45b2d-160">0x00000003</span><span class="sxs-lookup"><span data-stu-id="45b2d-160">0x00000003</span></span>  <br/> |
|<span data-ttu-id="45b2d-161">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="45b2d-161">MAPIOFFLINE_STATE_OFFLINE</span></span>  <br/> |<span data-ttu-id="45b2d-162">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45b2d-162">0x00000001</span></span>  <br/> |
|<span data-ttu-id="45b2d-163">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="45b2d-163">MAPIOFFLINE_STATE_ONLINE</span></span>  <br/> |<span data-ttu-id="45b2d-164">0x00000002</span><span class="sxs-lookup"><span data-stu-id="45b2d-164">0x00000002</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="45b2d-165">クラス識別子</span><span class="sxs-lookup"><span data-stu-id="45b2d-165">Class identifiers</span></span>

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a><span data-ttu-id="45b2d-166">インターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="45b2d-166">Interface identifiers</span></span>

```cpp
//{000672B5-0000-0000-c000-000000000046}
DEFINE_GUID(IID_IMAPIOffline, 0x000672B5, 0x0000, 0x0000, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
```

```cpp
//{0317bde5-fc29-44cd-8dcd-36125a3be9ec}
DEFINE_GUID(IID_IMAPIOfflineNotify, 0x0317bde5, 0xfc29, 0x44cd, 0x8d, 0xcd, 0x36, 0x12, 0x5a, 0x3b, 0xe9, 0xec);
```

```cpp
//{42175607-ff3e-4790-bc18-66c8643e6424
DEFINE_GUID(IID_IMAPIOfflineMgr, 0x42175607, 0xFF3E, 0x4790, 0xbc, 0x18, 0x66, 0xc8, 0x64, 0x3e, 0x64, 0x24);
```

## <a name="outlook-named-properties"></a><span data-ttu-id="45b2d-167">Outlook は名前付きプロパティ</span><span class="sxs-lookup"><span data-stu-id="45b2d-167">Outlook named properties</span></span>

<span data-ttu-id="45b2d-168">このセクションには、名前付きプロパティの定数の定義とその名前空間、およびその他の関連する定数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-168">This section contains constant definitions for named properties and their namespaces, and other related constants.</span></span>
  
### <a name="definitions-for-named-properties"></a><span data-ttu-id="45b2d-169">名前付きプロパティの定義</span><span class="sxs-lookup"><span data-stu-id="45b2d-169">Definitions for named properties</span></span>

```cpp
#define dispidMeetingType0x0026 
#define dispidFileUnder0x8005 
#define dispidYomiFirstName 0x802C 
#define dispidYomiLastName 0x802D 
#define dispidYomiCompanyName 0x802E 
#define dispidWorkAddressStreet 0x8045 
#define dispidWorkAddressCity 0x8046 
#define dispidWorkAddressState 0x8047 
#define dispidWorkAddressPostalCode 0x8048 
#define dispidWorkAddressCountry 0x8049 
#define dispidWorkAddressPostOfficeBox 0x804A 
#define dispidInstMsg 0x8062 
#define dispidEmailDisplayName 0x8080 
#define dispidEmailAddrType 0x8082 
#define dispidEmailEmailAddress 0x8083 
#define dispidEmailOriginalDisplayName 0x8084 
#define dispidEmail1OriginalEntryID0x8085 
#define dispidEmail2DisplayName 0x8090 
#define dispidEmail2AddrType 0x8092 
#define dispidEmail2EmailAddress 0x8093 
#define dispidEmail2OriginalDisplayName 0x8094 
#define dispidEmail2OriginalEntryID0x8095 
#define dispidEmail3DisplayName 0x80A0 
#define dispidEmail3AddrType 0x80A2 
#define dispidEmail3EmailAddress 0x80A3 
#define dispidEmail3OriginalDisplayName 0x80A4 
#define dispidEmail3OriginalEntryID0x80A5 
#define dispidTaskStatus 0x8101 
#define dispidTaskStartDate 0x8104 
#define dispidTaskDueDate 0x8105 
#define dispidTaskActualEffort 0x8110 
#define dispidTaskEstimatedEffort 0x8111 
#define dispidTaskFRecur 0x8126 
#define dispidBusyStatus0x8205 
#define dispidLocation 0x8208 
#define dispidApptStartWhole 0x820D 
#define dispidApptEndWhole 0x820E 
#define dispidApptDuration 0x8213 
#define dispidRecurring 0x8223 
#define dispidTimeZoneStruct0x8233 
#define dispidAllAttendeesString 0x8238 
#define dispidToAttendeesString 0x823B 
#define dispidCCAttendeesString 0x823C 
#define dispidConfCheck0x8240 
#define dispidApptCounterProposal 0x8257 
#define dispidApptTZDefStartDisplay0x825E 
#define dispidApptTZDefEndDisplay0x825F 
#define dispidApptTZDefRecur0x8260 
#define dispidReminderTime0x8502 
#define dispidReminderSet 0x8503 
#define dispidFormStorage0x850F 
#define dispidPageDirStream0x8513 
#define dispidSmartNoAttach 0x8514 
#define dispidCommonStart 0x8516 
#define dispidCommonEnd 0x8517 
#define dispidFormPropStream0x851B 
#define dispidRequest 0x8530 
#define dispidCompanies 0x8539 
#define dispidContacts0x853A 
#define dispidPropDefStream0x8540 
#define dispidScriptStream0x8541 
#define dispidCustomFlag0x8542 
#define dispidReminderNextTime 0x8560 
#define dispidHeaderItem0x8578 
#define dispidUseTNEF0x8582 
#define dispidToDoTitle0x85A4 
#define dispidLogType 0x8700 
#define dispidLogStart 0x8706 
#define dispidLogDuration 0x8707 
#define dispidLogEnd 0x8708 
```

### <a name="definitions-for-namespaces"></a><span data-ttu-id="45b2d-170">名前空間の定義</span><span class="sxs-lookup"><span data-stu-id="45b2d-170">Definitions for namespaces</span></span>

<span data-ttu-id="45b2d-171">次のグローバル一意識別子 (Guid) は、名前付きプロパティの名前空間を表します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-171">The following globally unique identifiers (GUIDs) represent the namespaces of the named properties.</span></span>
  
```cpp
const GUID PS_INTERNET_HEADERS  = {0x00020386, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PS_PUBLIC_STRINGS    = {0x00020329, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Appointment= {0x00062002, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Address       = {0x00062004, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Common        = {0x00062008, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Log           = {0x0006200A, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Meeting = {0x6ED8DA90, 0x450B, 0x101B, {0x98, 0xDA, 0x00, 0xAA, 0x00, 0x3F, 0x13, 0x05}}; 
const GUID PSETID_Task          = {0x00062003, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
```

<span data-ttu-id="45b2d-172">PSETID の定義は、MAPI ストアを参照してください。</span><span class="sxs-lookup"><span data-stu-id="45b2d-172">Refer to the section MAPI Store for the PSETID definitions.</span></span>
  
### <a name="other-constants"></a><span data-ttu-id="45b2d-173">他の定数</span><span class="sxs-lookup"><span data-stu-id="45b2d-173">Other constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45b2d-174">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="45b2d-174">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="45b2d-175">0xD000000</span><span class="sxs-lookup"><span data-stu-id="45b2d-175">0xD000000</span></span>  <br/> |
|<span data-ttu-id="45b2d-176">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="45b2d-176">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="45b2d-177">0x2000000</span><span class="sxs-lookup"><span data-stu-id="45b2d-177">0x2000000</span></span>  <br/> |
|<span data-ttu-id="45b2d-178">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="45b2d-178">MNID_ID</span></span>  <br/> | <span data-ttu-id="45b2d-179">*ヘッダー ファイルの mapidefs.h で定義します。*</span><span class="sxs-lookup"><span data-stu-id="45b2d-179">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="45b2d-180">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="45b2d-180">MNID_STRING</span></span>  <br/> | <span data-ttu-id="45b2d-181">*ヘッダー ファイルの mapidefs.h で定義します。*</span><span class="sxs-lookup"><span data-stu-id="45b2d-181">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="45b2d-182">mtgNone</span><span class="sxs-lookup"><span data-stu-id="45b2d-182">mtgNone</span></span>  <br/> |<span data-ttu-id="45b2d-183">0x0</span><span class="sxs-lookup"><span data-stu-id="45b2d-183">0x0</span></span>  <br/> |
|<span data-ttu-id="45b2d-184">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="45b2d-184">mtgRequest</span></span>  <br/> |<span data-ttu-id="45b2d-185">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45b2d-185">0x00000001</span></span>  <br/> |
|<span data-ttu-id="45b2d-186">mtgFullUpdate</span><span class="sxs-lookup"><span data-stu-id="45b2d-186">mtgFullUpdate</span></span>  <br/> |<span data-ttu-id="45b2d-187">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-187">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-188">mtgInfoUpdate</span><span class="sxs-lookup"><span data-stu-id="45b2d-188">mtgInfoUpdate</span></span>  <br/> |<span data-ttu-id="45b2d-189">0x00020000</span><span class="sxs-lookup"><span data-stu-id="45b2d-189">0x00020000</span></span>  <br/> |
|<span data-ttu-id="45b2d-190">mtgOutofDate</span><span class="sxs-lookup"><span data-stu-id="45b2d-190">mtgOutofDate</span></span>  <br/> |<span data-ttu-id="45b2d-191">0x00080000</span><span class="sxs-lookup"><span data-stu-id="45b2d-191">0x00080000</span></span>  <br/> |
|<span data-ttu-id="45b2d-192">mtgDelegated</span><span class="sxs-lookup"><span data-stu-id="45b2d-192">mtgDelegated</span></span>  <br/> |<span data-ttu-id="45b2d-193">0x00100000</span><span class="sxs-lookup"><span data-stu-id="45b2d-193">0x00100000</span></span>  <br/> |
   
## <a name="replication-api"></a><span data-ttu-id="45b2d-194">レプリケーション API</span><span class="sxs-lookup"><span data-stu-id="45b2d-194">Replication API</span></span>

<span data-ttu-id="45b2d-195">このセクションには、レプリケーション API の定数の定義、MAPI インターフェイスの宣言、およびクラス識別子とインターフェイス識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-195">This section contains constant definitions, MAPI interface declarations, and class and interface identifiers for the Replication API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="45b2d-196">定数</span><span class="sxs-lookup"><span data-stu-id="45b2d-196">Constants</span></span>

<span data-ttu-id="45b2d-197">MAPI サービス プロバイダーを識別する[MAPIUID](mapiuid.md)構造体は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="45b2d-197">The following is a [MAPIUID](mapiuid.md) structure identifying a MAPI service provider:</span></span> 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|<span data-ttu-id="45b2d-198">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-198">DNH_OK</span></span>  <br/> |<span data-ttu-id="45b2d-199">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-199">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-200">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-200">DNT_OK</span></span>  <br/> |<span data-ttu-id="45b2d-201">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-201">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-202">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="45b2d-202">HSF_LOCAL</span></span>  <br/> |<span data-ttu-id="45b2d-203">0x00000008</span><span class="sxs-lookup"><span data-stu-id="45b2d-203">0x00000008</span></span>  <br/> |
|<span data-ttu-id="45b2d-204">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="45b2d-204">HSF_COPYDESTRUCTIVE</span></span>  <br/> |<span data-ttu-id="45b2d-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45b2d-205">0x00000010</span></span>  <br/> |
|<span data-ttu-id="45b2d-206">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-206">HSF_OK</span></span>  <br/> |<span data-ttu-id="45b2d-207">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-207">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-208">MDB_OST_LOGON_UNICODE</span><span class="sxs-lookup"><span data-stu-id="45b2d-208">MDB_OST_LOGON_UNICODE</span></span>  <br/> |<span data-ttu-id="45b2d-209">((ULONG) 0X00000800)</span><span class="sxs-lookup"><span data-stu-id="45b2d-209">((ULONG) 0x00000800)</span></span>  <br/> |
|<span data-ttu-id="45b2d-210">MDB_OST_LOGON_ANSI</span><span class="sxs-lookup"><span data-stu-id="45b2d-210">MDB_OST_LOGON_ANSI</span></span>  <br/> |<span data-ttu-id="45b2d-211">((ULONG) 0X00001000)</span><span class="sxs-lookup"><span data-stu-id="45b2d-211">((ULONG) 0x00001000)</span></span>  <br/> |
|<span data-ttu-id="45b2d-212">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="45b2d-212">SHOW_SOFT_DELETES</span></span>  <br/> |<span data-ttu-id="45b2d-213">((ULONG) 0X00000002)</span><span class="sxs-lookup"><span data-stu-id="45b2d-213">((ULONG) 0x00000002)</span></span>  <br/> |
|<span data-ttu-id="45b2d-214">SS_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="45b2d-214">SS_ACTIVE</span></span>  <br/> |<span data-ttu-id="45b2d-215">0</span><span class="sxs-lookup"><span data-stu-id="45b2d-215">0</span></span>  <br/> |
|<span data-ttu-id="45b2d-216">SS_SUSPENDED</span><span class="sxs-lookup"><span data-stu-id="45b2d-216">SS_SUSPENDED</span></span>  <br/> |<span data-ttu-id="45b2d-217">1</span><span class="sxs-lookup"><span data-stu-id="45b2d-217">1</span></span>  <br/> |
|<span data-ttu-id="45b2d-218">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="45b2d-218">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="45b2d-219">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45b2d-219">0x00000001</span></span>  <br/> |
|<span data-ttu-id="45b2d-220">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="45b2d-220">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="45b2d-221">0x00000002</span><span class="sxs-lookup"><span data-stu-id="45b2d-221">0x00000002</span></span>  <br/> |
|<span data-ttu-id="45b2d-222">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="45b2d-222">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="45b2d-223">0x00000040</span><span class="sxs-lookup"><span data-stu-id="45b2d-223">0x00000040</span></span>  <br/> |
|<span data-ttu-id="45b2d-224">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="45b2d-224">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="45b2d-225">0x00000080</span><span class="sxs-lookup"><span data-stu-id="45b2d-225">0x00000080</span></span>  <br/> |
|<span data-ttu-id="45b2d-226">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="45b2d-226">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="45b2d-227">0x00000200</span><span class="sxs-lookup"><span data-stu-id="45b2d-227">0x00000200</span></span>  <br/> |
|<span data-ttu-id="45b2d-228">SYNC_BACKGROUND</span><span class="sxs-lookup"><span data-stu-id="45b2d-228">SYNC_BACKGROUND</span></span>  <br/> |<span data-ttu-id="45b2d-229">0x00001000</span><span class="sxs-lookup"><span data-stu-id="45b2d-229">0x00001000</span></span>  <br/> |
|<span data-ttu-id="45b2d-230">SYNC_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="45b2d-230">SYNC_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="45b2d-231">0x00020000</span><span class="sxs-lookup"><span data-stu-id="45b2d-231">0x00020000</span></span>  <br/> |
|<span data-ttu-id="45b2d-232">SYNC_HEADERS</span><span class="sxs-lookup"><span data-stu-id="45b2d-232">SYNC_HEADERS</span></span>  <br/> |<span data-ttu-id="45b2d-233">0x02000000</span><span class="sxs-lookup"><span data-stu-id="45b2d-233">0x02000000</span></span>  <br/> |
|<span data-ttu-id="45b2d-234">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-234">UPC_OK</span></span>  <br/> |<span data-ttu-id="45b2d-235">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-235">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-236">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="45b2d-236">UPD_ASSOC</span></span>  <br/> |<span data-ttu-id="45b2d-237">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45b2d-237">0x00000001</span></span>  <br/> |
|<span data-ttu-id="45b2d-238">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="45b2d-238">UPD_MOV</span></span>  <br/> |<span data-ttu-id="45b2d-239">0x00000002</span><span class="sxs-lookup"><span data-stu-id="45b2d-239">0x00000002</span></span>  <br/> |
|<span data-ttu-id="45b2d-240">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-240">UPD_OK</span></span>  <br/> |<span data-ttu-id="45b2d-241">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-241">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-242">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="45b2d-242">UPD_MOVED</span></span>  <br/> |<span data-ttu-id="45b2d-243">0x00020000</span><span class="sxs-lookup"><span data-stu-id="45b2d-243">0x00020000</span></span>  <br/> |
|<span data-ttu-id="45b2d-244">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="45b2d-244">UPD_UPDATE</span></span>  <br/> |<span data-ttu-id="45b2d-245">0x00040000</span><span class="sxs-lookup"><span data-stu-id="45b2d-245">0x00040000</span></span>  <br/> |
|<span data-ttu-id="45b2d-246">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="45b2d-246">UPD_COMMIT</span></span>  <br/> |<span data-ttu-id="45b2d-247">0x00080000</span><span class="sxs-lookup"><span data-stu-id="45b2d-247">0x00080000</span></span>  <br/> |
|<span data-ttu-id="45b2d-248">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="45b2d-248">UPF_NEW</span></span>  <br/> |<span data-ttu-id="45b2d-249">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45b2d-249">0x00000001</span></span>  <br/> |
|<span data-ttu-id="45b2d-250">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="45b2d-250">UPF_MOD_PARENT</span></span>  <br/> |<span data-ttu-id="45b2d-251">0x00000002</span><span class="sxs-lookup"><span data-stu-id="45b2d-251">0x00000002</span></span>  <br/> |
|<span data-ttu-id="45b2d-252">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="45b2d-252">UPF_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="45b2d-253">0x00000004</span><span class="sxs-lookup"><span data-stu-id="45b2d-253">0x00000004</span></span>  <br/> |
|<span data-ttu-id="45b2d-254">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="45b2d-254">UPF_DEL</span></span>  <br/> |<span data-ttu-id="45b2d-255">0x00000008</span><span class="sxs-lookup"><span data-stu-id="45b2d-255">0x00000008</span></span>  <br/> |
|<span data-ttu-id="45b2d-256">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-256">UPF_OK</span></span>  <br/> |<span data-ttu-id="45b2d-257">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-257">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-258">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-258">UPH_OK</span></span>  <br/> |<span data-ttu-id="45b2d-259">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-259">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-260">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="45b2d-260">UPM_ASSOC</span></span>  <br/> |<span data-ttu-id="45b2d-261">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45b2d-261">0x00000001</span></span>  <br/> |
|<span data-ttu-id="45b2d-262">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="45b2d-262">UPM_NEW</span></span>  <br/> |<span data-ttu-id="45b2d-263">0x00000002</span><span class="sxs-lookup"><span data-stu-id="45b2d-263">0x00000002</span></span>  <br/> |
|<span data-ttu-id="45b2d-264">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="45b2d-264">UPM_MOV</span></span>  <br/> |<span data-ttu-id="45b2d-265">0x00000004</span><span class="sxs-lookup"><span data-stu-id="45b2d-265">0x00000004</span></span>  <br/> |
|<span data-ttu-id="45b2d-266">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="45b2d-266">UPM_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="45b2d-267">0x00000008</span><span class="sxs-lookup"><span data-stu-id="45b2d-267">0x00000008</span></span>  <br/> |
|<span data-ttu-id="45b2d-268">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="45b2d-268">UPM_HEADER</span></span>  <br/> |<span data-ttu-id="45b2d-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45b2d-269">0x00000010</span></span>  <br/> |
|<span data-ttu-id="45b2d-270">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-270">UPM_OK</span></span>  <br/> |<span data-ttu-id="45b2d-271">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-271">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-272">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="45b2d-272">UPM_MOVED</span></span>  <br/> |<span data-ttu-id="45b2d-273">0x00020000</span><span class="sxs-lookup"><span data-stu-id="45b2d-273">0x00020000</span></span>  <br/> |
|<span data-ttu-id="45b2d-274">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="45b2d-274">UPM_COMMIT</span></span>  <br/> |<span data-ttu-id="45b2d-275">0x00040000</span><span class="sxs-lookup"><span data-stu-id="45b2d-275">0x00040000</span></span>  <br/> |
|<span data-ttu-id="45b2d-276">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="45b2d-276">UPM_DELETE</span></span>  <br/> |<span data-ttu-id="45b2d-277">0x00080000</span><span class="sxs-lookup"><span data-stu-id="45b2d-277">0x00080000</span></span>  <br/> |
|<span data-ttu-id="45b2d-278">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="45b2d-278">UPM_SAVE</span></span>  <br/> |<span data-ttu-id="45b2d-279">0x00100000</span><span class="sxs-lookup"><span data-stu-id="45b2d-279">0x00100000</span></span>  <br/> |
|<span data-ttu-id="45b2d-280">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="45b2d-280">UPR_ASSOC</span></span>  <br/> |<span data-ttu-id="45b2d-281">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45b2d-281">0x00000001</span></span>  <br/> |
|<span data-ttu-id="45b2d-282">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="45b2d-282">UPR_READ</span></span>  <br/> |<span data-ttu-id="45b2d-283">0x00000002</span><span class="sxs-lookup"><span data-stu-id="45b2d-283">0x00000002</span></span>  <br/> |
|<span data-ttu-id="45b2d-284">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-284">UPR_OK</span></span>  <br/> |<span data-ttu-id="45b2d-285">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-285">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-286">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="45b2d-286">UPR_COMMIT</span></span>  <br/> |<span data-ttu-id="45b2d-287">0x00020000</span><span class="sxs-lookup"><span data-stu-id="45b2d-287">0x00020000</span></span>  <br/> |
|<span data-ttu-id="45b2d-288">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="45b2d-288">UPS_UPLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="45b2d-289">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45b2d-289">0x00000001</span></span>  <br/> |
|<span data-ttu-id="45b2d-290">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="45b2d-290">UPS_DNLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="45b2d-291">0x00000002</span><span class="sxs-lookup"><span data-stu-id="45b2d-291">0x00000002</span></span>  <br/> |
|<span data-ttu-id="45b2d-292">UPS_ONE_FOLDER</span><span class="sxs-lookup"><span data-stu-id="45b2d-292">UPS_ONE_FOLDER</span></span>  <br/> |<span data-ttu-id="45b2d-293">0x00000004</span><span class="sxs-lookup"><span data-stu-id="45b2d-293">0x00000004</span></span>  <br/> |
|<span data-ttu-id="45b2d-294">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="45b2d-294">UPS_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="45b2d-295">0x00000080</span><span class="sxs-lookup"><span data-stu-id="45b2d-295">0x00000080</span></span>  <br/> |
|<span data-ttu-id="45b2d-296">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-296">UPS_OK</span></span>  <br/> |<span data-ttu-id="45b2d-297">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-297">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-298">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-298">UPT_OK</span></span>  <br/> |<span data-ttu-id="45b2d-299">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-299">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-300">UPT_PUBLIC</span><span class="sxs-lookup"><span data-stu-id="45b2d-300">UPT_PUBLIC</span></span>  <br/> |<span data-ttu-id="45b2d-301">0x00000001</span><span class="sxs-lookup"><span data-stu-id="45b2d-301">0x00000001</span></span>  <br/> |
|<span data-ttu-id="45b2d-302">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="45b2d-302">UPV_ERROR</span></span>  <br/> |<span data-ttu-id="45b2d-303">0x00010000</span><span class="sxs-lookup"><span data-stu-id="45b2d-303">0x00010000</span></span>  <br/> |
|<span data-ttu-id="45b2d-304">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="45b2d-304">UPV_DIRTY</span></span>  <br/> |<span data-ttu-id="45b2d-305">0x00020000</span><span class="sxs-lookup"><span data-stu-id="45b2d-305">0x00020000</span></span>  <br/> |
|<span data-ttu-id="45b2d-306">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="45b2d-306">UPV_COMMIT</span></span>  <br/> |<span data-ttu-id="45b2d-307">0x00040000</span><span class="sxs-lookup"><span data-stu-id="45b2d-307">0x00040000</span></span>  <br/> |
   
### <a name="interface-declarations"></a><span data-ttu-id="45b2d-308">インターフェイスの宣言</span><span class="sxs-lookup"><span data-stu-id="45b2d-308">Interface declarations</span></span>

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a><span data-ttu-id="45b2d-309">インターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="45b2d-309">Interface identifiers</span></span>

```cpp
//{4FDEEFF0-0319-11CF-B4CF-00AA0DBBB6E6}
DEFINE_GUID (IID_IPSTX, 0x4FDEEFF0, 0x0319, 0x11CF, 0xB4, 0xCF, 0x00, 0xAA, 0x0D, 0xBB, 0xB6, 0xE6)
```

```cpp
//{2067A790-2A45-11D1-EB86-00A0C90DCA6D}
DEFINE_GUID (IID_IPSTX2, 0x2067A790, 0x2A45, 0x11D1, 0xEB, 0x86, 0x00, 0xA0, 0xC9, 0x0D, 0xCA, 0x6D)
```

```cpp
//{55f15320-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX3, 0x55f15320, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{aa2e2092-ac08-11d2-a2f9-0060b0ec3d4f}
DEFINE_GUID (IID_IPSTX4, 0xaa2e2092, 0xac08, 0x11d2, 0xa2, 0xf9, 0x00, 0x60, 0xb0, 0xec, 0x3d, 0x4f)
```

```cpp
//{55f15322-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX5, 0x55f15322, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{55f15323-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX6, 0x55f15323, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{d2d85db4-840f-49b8-9982-07d2405ec6b7}
DEFINE_GUID (IID_IOSTX, 0xd2d85db4,  0x840f, 0x49b8, 0x99, 0x82, 0x07, 0xd2, 0x40, 0x5e, 0xc6, 0xb7)
```

<br/>

<span data-ttu-id="45b2d-310">[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)、 [IMAPISession::OpenEntry](imapisession-openentry.md)、または[IMsgStore::OpenEntry](imsgstore-openentry.md)を開き、それぞれのフォルダー オブジェクトとメッセージ オブジェクトのいずれかのプロバイダー チェックを無視して次の 2 つのインターフェイス識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-310">Use the two following interface identifiers with [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), or [IMsgStore::OpenEntry](imsgstore-openentry.md) to open and ignore any provider check on a folder object and a message object, respectively.</span></span> 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a><span data-ttu-id="45b2d-311">MAPI ストア</span><span class="sxs-lookup"><span data-stu-id="45b2d-311">MAPI store</span></span>

<span data-ttu-id="45b2d-312">このセクションには、定数の定義が含まれています、インタ フェース識別子によって使用 Api インターフェイス MAPI ストアを持つ。</span><span class="sxs-lookup"><span data-stu-id="45b2d-312">This section contains constant definitions and interface identifiers used by APIs that interface with a MAPI store.</span></span>
  
### <a name="constants"></a><span data-ttu-id="45b2d-313">定数</span><span class="sxs-lookup"><span data-stu-id="45b2d-313">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="45b2d-314">fnevIndexing</span><span class="sxs-lookup"><span data-stu-id="45b2d-314">fnevIndexing</span></span>  <br/> |<span data-ttu-id="45b2d-315">((ULONG) 0X00010000)</span><span class="sxs-lookup"><span data-stu-id="45b2d-315">((ULONG) 0x00010000)</span></span>  <br/> |<span data-ttu-id="45b2d-316">ストア プロバイダーは、オブジェクトがインデックス作成の準備が完了であることをインデクサーに通知する**[通知](notification.md)** の構造体の**ulEventType**メンバーに**fnevIndexing**を指定できます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-316">A store provider can specify **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure to notify the indexer that an object is ready for indexing.</span></span> <span data-ttu-id="45b2d-317">**通知**の構造体のメンバー**情報**には、 **[EXTENDED_NOTIFICATION](extended_notification.md)** 構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-317">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="45b2d-318">FS_NONE</span><span class="sxs-lookup"><span data-stu-id="45b2d-318">FS_NONE</span></span>  <br/> |<span data-ttu-id="45b2d-319">0x00</span><span class="sxs-lookup"><span data-stu-id="45b2d-319">0x00</span></span>  <br/> |<span data-ttu-id="45b2d-320">クライアントは、返されるビットマスクの**[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** とチェックを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-320">A client can call **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** and check for the returned bitmask.</span></span> <span data-ttu-id="45b2d-321">**FS_NONE**は、フォルダーを共有するサポートしていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-321">**FS_NONE** indicates that the folder does not support sharing.</span></span>  <br/> |
|<span data-ttu-id="45b2d-322">FS_SUPPORTS_SHARING</span><span class="sxs-lookup"><span data-stu-id="45b2d-322">FS_SUPPORTS_SHARING</span></span>  <br/> |<span data-ttu-id="45b2d-323">0x01</span><span class="sxs-lookup"><span data-stu-id="45b2d-323">0x01</span></span>  <br/> |<span data-ttu-id="45b2d-324">クライアントは、返されるビットマスクの**IFolderSupport::GetSupportMask**とチェックを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-324">A client can call **IFolderSupport::GetSupportMask** and check for the returned bitmask.</span></span> <span data-ttu-id="45b2d-325">**FS_SUPPORTS_SHARING**では、共有フォルダーをサポートしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-325">**FS_SUPPORTS_SHARING** indicates that the folder supports sharing.</span></span>  <br/> |
|<span data-ttu-id="45b2d-326">INDEXING_SEARCH_OWNER</span><span class="sxs-lookup"><span data-stu-id="45b2d-326">INDEXING_SEARCH_OWNER</span></span>  <br/> |<span data-ttu-id="45b2d-327">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="45b2d-327">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="45b2d-328">させようとして、通知オブジェクトは、インデックス作成の準備ができて、インデクサーのプロセスを識別します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-328">Identifies the process that is pushing a notification to an indexer that an object is ready for indexing.</span></span>  <br/> |
|<span data-ttu-id="45b2d-329">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="45b2d-329">MNID_ID</span></span>  <br/> |<span data-ttu-id="45b2d-330">Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル mapidefs.h に定義されています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-330">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h</span></span>  <br/> |<span data-ttu-id="45b2d-331">**UlKind** 、 **[MAPINAMEID](mapinameid.md)** 構造体のフィールドの値です。</span><span class="sxs-lookup"><span data-stu-id="45b2d-331">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="45b2d-332">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="45b2d-332">MNID_STRING</span></span>  <br/> |<span data-ttu-id="45b2d-333">Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル mapidefs.h で定義します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-333">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h.</span></span>  <br/> |<span data-ttu-id="45b2d-334">**UlKind** 、 **[MAPINAMEID](mapinameid.md)** 構造体のフィールドの値です。</span><span class="sxs-lookup"><span data-stu-id="45b2d-334">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="45b2d-335">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="45b2d-335">MSCAP_RES_ANNOTATION</span></span>  <br/> |<span data-ttu-id="45b2d-336">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="45b2d-336">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="45b2d-337">クライアントは、 **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)** の*mscapSelector*で**MSCAP_SEL_RESTRICTION**を指定する場合**GetCapabilities**は、ストアは、制限の中で無効なパラメーターを無視する場合にこの値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-337">If a client specifies **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  for **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** can return this value if the store ignores invalid parameters in a restriction.</span></span>  <br/> |
|<span data-ttu-id="45b2d-338">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="45b2d-338">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>  <br/> |<span data-ttu-id="45b2d-339">((ULONG) 0X00000020)</span><span class="sxs-lookup"><span data-stu-id="45b2d-339">((ULONG) 0x00000020)</span></span>  <br/> |<span data-ttu-id="45b2d-340">クライアントは、 **IMSCapabilities::GetCapabilities**の*mscapSelector*で**MSCAP_SEL_FOLDER**を指定した場合、 **GetCapabilities**はストアがフォルダーのホーム ページをサポートする既定以外のストアである場合にこの値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-340">If a client specifies **MSCAP_SEL_FOLDER** in  *mscapSelector*  for **IMSCapabilities::GetCapabilities**, **GetCapabilities** can return this value if the store is a non-default store that supports folder home pages.</span></span>  <br/> |
|<span data-ttu-id="45b2d-341">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-341">STORE_PUSHER_OK</span></span>  <br/> |<span data-ttu-id="45b2d-342">((ULONG) 0X00800000)</span><span class="sxs-lookup"><span data-stu-id="45b2d-342">((ULONG) 0x00800000)</span></span>  <br/> |<span data-ttu-id="45b2d-343">クライアントは、メッセージ ・ ストアの特性を決定する**[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** プロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-343">A client can get the property **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** to determine the characteristic of a message store.</span></span> <span data-ttu-id="45b2d-344">ストア プロバイダーは、ビットマスク内の**STORE_PUSHER_OK**フラグを設定、MAPI プロトコル ハンドラーはストアをクロールしないと、ストアは、メッセージのインデックスを作成するのにはインデクサーに通知を使用して、変更をプッシュすることを意味します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-344">If the store provider sets the **STORE_PUSHER_OK** flag in the bitmask, that means the MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>  <br/> |
   
### <a name="definitions-for-namespaces"></a><span data-ttu-id="45b2d-345">名前空間の定義</span><span class="sxs-lookup"><span data-stu-id="45b2d-345">Definitions for namespaces</span></span>

<span data-ttu-id="45b2d-346">次のグローバル一意識別子 (Guid) は、名前付きプロパティの名前空間を表します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-346">The following globally unique identifiers (GUIDs) represent the namespaces of named properties.</span></span> <span data-ttu-id="45b2d-347">MAPI プロトコル ハンドラー (PH) では、インデックスを作成、読み取り専用として記載されています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-347">They are indexed by the MAPI Protocol Handler (PH), and are documented as read-only.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="45b2d-348">作成または項目を変更する名前付きプロパティを使用してくださいできません。</span><span class="sxs-lookup"><span data-stu-id="45b2d-348">The named properties should not be used to create or modify items.</span></span> 
  
```cpp
const GUID PS_INTERNET_HEADERS  = {0x00020386, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PS_PUBLIC_STRINGS    = {0x00020329, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Address       = {0x00062004, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Appointment   = {0x00062002, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Common        = {0x00062008, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Log           = {0x0006200A, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Meeting       = {0x6ED8DA90, 0x450B, 0x101B, {0x98, 0xDA, 0x00, 0xAA, 0x00, 0x3F, 0x13, 0x05}}; 
const GUID PSETID_Task          = {0x00062003, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
```

#### <a name="mnidid-properties"></a><span data-ttu-id="45b2d-349">MNID_ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="45b2d-349">MNID_ID Properties</span></span>
  
```cpp
// In PSETID_Address
#define dispidWorkAddressStreet 0x8045
#define dispidWorkAddressCity 0x8046
#define dispidWorkAddressState 0x8047
#define dispidWorkAddressPostalCode 0x8048
#define dispidWorkAddressCountry 0x8049
#define dispidInstMsg 0x8062
#define dispidEmailDisplayName 0x8080
#define dispidEmailOriginalDisplayName 0x8084
```

```cpp
// In PSETID_Appointment
#define dispidLocation 0x8208
#define dispidApptStartWhole 0x820D
#define dispidApptEndWhole 0x820E
#define dispidApptDuration 0x8213
#define dispidRecurring 0x8223
#define dispidAllAttendeesString 0x8238
#define dispidToAttendeesString 0x823B
#define dispidCCAttendeesString 0x823C
```

```cpp
// In PSETID_Common
#define dispidReminderSet 0x8503
#define dispidSmartNoAttach 0x8514
#define dispidCommonStart 0x8516
#define dispidCommonEnd 0x8517
#define dispidRequest 0x8530
#define dispidCompanies 0x8539
#define dispidReminderNextTime 0x8560
```

```cpp
// In PSETID_Log (also known as Journal)
#define dispidLogType 0x8700
#define dispidLogStart 0x8706
#define dispidLogDuration 0x8707
#define dispidLogEnd 0x8708MNID_STRING properties
```

```cpp
// In PSETID_Task
#define dispidTaskStartDate 0x8104
#define dispidTaskDueDate 0x8105
#define dispidTaskActualEffort 0x8110
#define dispidTaskEstimatedEffort 0x8111
#define dispidTaskFRecur 0x8126
```

#### <a name="mnidstring-properties"></a><span data-ttu-id="45b2d-350">MNID_STRING プロパティ</span><span class="sxs-lookup"><span data-stu-id="45b2d-350">MNID_STRING Properties</span></span>
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a><span data-ttu-id="45b2d-351">インターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="45b2d-351">Interface identifiers</span></span>

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

<span data-ttu-id="45b2d-352">使用して、`DEFINE_OLEGUID`の値で、次の GUID のシンボリック名を関連付けるには、Windows SDK ヘッダー ファイル guiddef.h に定義されているマクロ。</span><span class="sxs-lookup"><span data-stu-id="45b2d-352">Use the  `DEFINE_OLEGUID` macro defined in the Windows SDK header file guiddef.h to associate the following GUID symbolic name with its value.</span></span> 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a><span data-ttu-id="45b2d-353">MAPI アドレス帳の定数</span><span class="sxs-lookup"><span data-stu-id="45b2d-353">MAPI Address Book constants</span></span>

<span data-ttu-id="45b2d-354">このセクションには、MAPI アドレス帳の定数の定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-354">This section contains constant definitions for the MAPI Address Book.</span></span>
  
### <a name="constants"></a><span data-ttu-id="45b2d-355">定数</span><span class="sxs-lookup"><span data-stu-id="45b2d-355">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="45b2d-356">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="45b2d-356">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="45b2d-357">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="45b2d-357">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="45b2d-358">MAPI アドレス帳オブジェクトのルート フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="45b2d-358">The root folder for a MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="45b2d-359">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="45b2d-359">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="45b2d-360">((ULONG) 0X00000002)</span><span class="sxs-lookup"><span data-stu-id="45b2d-360">((ULONG) 0x00000002)</span></span>  <br/> |<span data-ttu-id="45b2d-361">MAPI アドレス帳のオブジェクトのルート フォルダー内に含まれるサブフォルダー。</span><span class="sxs-lookup"><span data-stu-id="45b2d-361">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="45b2d-362">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="45b2d-362">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="45b2d-363">((ULONG) 0X00000003)</span><span class="sxs-lookup"><span data-stu-id="45b2d-363">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="45b2d-364">�A�h���X���̃R���e�i�[ �I�u�W�F�N�g�ł��B</span><span class="sxs-lookup"><span data-stu-id="45b2d-364">An address book container object.</span></span>  <br/> |
|<span data-ttu-id="45b2d-365">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="45b2d-365">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="45b2d-366">((ULONG) 0X00000004)</span><span class="sxs-lookup"><span data-stu-id="45b2d-366">((ULONG) 0x00000004)</span></span>  <br/> |<span data-ttu-id="45b2d-367">���b�Z�[�W���O ���[�U�[ �I�u�W�F�N�g�ł��B</span><span class="sxs-lookup"><span data-stu-id="45b2d-367">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="45b2d-368">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="45b2d-368">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="45b2d-369">((ULONG) 0X00000005)</span><span class="sxs-lookup"><span data-stu-id="45b2d-369">((ULONG) 0x00000005)</span></span>  <br/> |<span data-ttu-id="45b2d-370">�z�z���X�g �I�u�W�F�N�g�ł��B</span><span class="sxs-lookup"><span data-stu-id="45b2d-370">A distribution list object.</span></span>  <br/> |
   
## <a name="additional-mapi-constants"></a><span data-ttu-id="45b2d-371">追加の MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="45b2d-371">Additional MAPI constants</span></span>

<span data-ttu-id="45b2d-372">このセクションには、エラー コード、および公開され文書化されていない MAPI Api で使用されるインターフェイス識別子を含む定数の定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-372">This section contains constant definitions including error codes, and interface identifiers used by MAPI APIs that were not previously exposed and documented.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="45b2d-373">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="45b2d-373">DIALOG_MODAL</span></span>  <br/> |<span data-ttu-id="45b2d-374">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="45b2d-374">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="45b2d-375">クライアントが[IAddrBook::Details](iaddrbook-details.md)メソッドを呼び出すと、クライアントは、 _ulFlags_パラメーターを特定のアドレス帳のエントリに関する詳細を表示するモーダル ダイアログ ボックスを表示するに**DIALOG_MODAL**フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45b2d-375">When a client calls the [IAddrBook::Details](iaddrbook-details.md) method, the client must set the **DIALOG_MODAL** flag in the  _ulFlags_ parameter to display the modal dialog box showing the details about a particular address book entry.</span></span> <span data-ttu-id="45b2d-376">この定数は、mapidefs.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-376">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="45b2d-377">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="45b2d-377">ITEMPROC_FORCE</span></span>  <br/> |<span data-ttu-id="45b2d-378">0x00000800</span><span class="sxs-lookup"><span data-stu-id="45b2d-378">0x00000800</span></span>  <br/> |<span data-ttu-id="45b2d-379">Outlook 2007 では、ラップされた PST ストアがルールにあり、MAPI クライアントは、新しいメッセージの通知を受け取る前に新しいメッセージ スパム フィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-379">In Outlook 2007, wrapped PST stores have rules and spam filtering processed on new messages before MAPI clients are notified of the new messages.</span></span> <span data-ttu-id="45b2d-380">プロバイダーまたは PST ストアで新しいメッセージを作成するのには、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを使用してクライアントは、 _ulFlags_メソッドのパラメーターに、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md) PST に示すために**ITEMPROC_FORCE**フラグを設定する必要があります。ストアは、メッセージの対象とする規則をストアが、新しいメッセージの到着をリッスンしているすべてのクライアントに通知する前に処理します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-380">A provider or client using the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new message in PST stores should set the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to indicate to the PST store that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="45b2d-381">Exchange Server がサーバー上のメッセージのルールを処理するために Microsoft Exchange Server ではないサーバー上で作成された新しいメッセージだけを処理するこのような規則が適用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="45b2d-381">Note that such rules processing only applies to new messages created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="45b2d-382">したがって、プロバイダーまたはメッセージを作成するクライアントは、 **NON_EMS_XP_SAVE**サーバーが Exchange サーバーではないことを示すとの組み合わせでこのフラグを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="45b2d-382">Hence the provider or client creating the message must pass this flag in combination with **NON_EMS_XP_SAVE**, which indicates the server is not an Exchange server.</span></span>  <br/> |
| <span data-ttu-id="45b2d-383">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="45b2d-383">MAPI_BG_SESSION</span></span>  <br/> |<span data-ttu-id="45b2d-384">0x00200000</span><span class="sxs-lookup"><span data-stu-id="45b2d-384">0x00200000</span></span>  <br/> |<span data-ttu-id="45b2d-385">クライアントは、セッションにログオンし、バック グラウンドで任意の操作を実行するには、 _flFlags_パラメーターで**MAPI_BG_SESSION**フラグを設定、 [MAPILogonEx](mapilogonex.md)関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-385">A client can call the [MAPILogonEx](mapilogonex.md) function, setting the **MAPI_BG_SESSION** flag in the  _flFlags_ parameter to log on to a session and carry out any operations in the background.</span></span> <span data-ttu-id="45b2d-386">一般に、クライアントがバック グラウンド スレッドかフォア グラウンド スレッドに目障りではない方法で別のプロセスでの処理を実行しようとすると場合、は、 **MAPI_BG_SESSION**フラグを使用して[MAPILogonEx](mapilogonex.md)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="45b2d-386">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call [MAPILogonEx](mapilogonex.md) with the **MAPI_BG_SESSION** flag.</span></span> <span data-ttu-id="45b2d-387">これが使用されている例は、バック グラウンドのアクセス権の種類の個人用フォルダー ファイル (PST) を開く、インデックス エンジンなど、クライアント アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="45b2d-387">An example where this is used is a client application, such as an indexing engine, opening a Personal Folders File (PST) for background type access.</span></span>  <br/> |
|<span data-ttu-id="45b2d-388">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="45b2d-388">MAPI_CACHE_ONLY</span></span>  <br/> |<span data-ttu-id="45b2d-389">0x00004000</span><span class="sxs-lookup"><span data-stu-id="45b2d-389">0x00004000</span></span>  <br/> |<span data-ttu-id="45b2d-390">クライアントは、 _ulFlags_パラメーター エントリをアドレス帳を開くと、キャッシュからのみ、その後にアクセスするために**MAPI_CACHE_ONLY**フラグを設定、[アドレス帳コンテナー](iaddrbook-openentry.md)のメソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-390">A client can call the [IAddrBook::OpenEntry](iaddrbook-openentry.md) method, setting the **MAPI_CACHE_ONLY** flag in the  _ulFlags_ parameter to open an address book entry and to access it subsequently only from the cache.</span></span> <span data-ttu-id="45b2d-391">これが使用されている例は、Exchange キャッシュ モードでグローバル アドレス一覧を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスしようとしているクライアント アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="45b2d-391">An example where this is used is a client application that wants to open the Global Address List in Cached Exchange mode and access an entry in that Address Book from the cache without creating traffic between the client and the server.</span></span>  <br/> |
|<span data-ttu-id="45b2d-392">MAPI_DIALOG_MODELESS</span><span class="sxs-lookup"><span data-stu-id="45b2d-392">MAPI_DIALOG_MODELESS</span></span>  <br/> |<span data-ttu-id="45b2d-393">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="45b2d-393">0x0000000C</span></span>  <br/> |<span data-ttu-id="45b2d-394">_UlFlags_パラメーターで既定の電子メール アプリケーションにモードレス ダイアログ ボックスが表示されることを指定するには、簡易 MAPI MAPISendMail 関数には、この値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-394">This value can be passed to the Simple MAPI MAPISendMail function in the  _ulFlags_ parameter to specify that a modeless dialog box is displayed by the default mail application.</span></span> <span data-ttu-id="45b2d-395">このフラグも MAPI_DIALOG (0x00000008) が設定されている場合、ダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="45b2d-395">If neither this flag nor MAPI_DIALOG (0x00000008) is set, no dialog box is displayed.</span></span>  <br/> |
|<span data-ttu-id="45b2d-396">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="45b2d-396">MAPI_NO_CACHE</span></span>  <br/> |<span data-ttu-id="45b2d-397">0x00000200</span><span class="sxs-lookup"><span data-stu-id="45b2d-397">0x00000200</span></span>  <br/> |<span data-ttu-id="45b2d-398">Microsoft Office Outlook が Exchange キャッシュ モードでは、ストアは、キャッシュ モードで開かれていた場合は、クライアントまたはサービス プロバイダーが[IMsgStore::OpenEntry](imsgstore-openentry.md)、 **MAPI_NO_CACHE**フラグを設定して、 _ulFlags_に渡すパラメーターでアイテムを開くを呼び出すことができますか、リモート ストア上のフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="45b2d-398">If Microsoft Office Outlook is in Cached Exchange Mode and a store has been opened in cached mode, a client or service provider can call [IMsgStore::OpenEntry](imsgstore-openentry.md), setting the **MAPI_NO_CACHE** flag in the  _ulFlags_ parameter to open an item or a folder on the remote store.</span></span> <span data-ttu-id="45b2d-399">場合は、メッセージ ストアを開くには、リモート サーバー上で**MDB_ONLINE**フラグを使用して、必要はありません**MAPI_NO_CACHE**フラグを使用するに注意してください。</span><span class="sxs-lookup"><span data-stu-id="45b2d-399">Note that if you open the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span>  <br/> |
|<span data-ttu-id="45b2d-400">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="45b2d-400">MAPI_UNICODE</span></span>  <br/> |<span data-ttu-id="45b2d-401">0x80000000</span><span class="sxs-lookup"><span data-stu-id="45b2d-401">0x80000000</span></span>  <br/> |<span data-ttu-id="45b2d-402">クライアントまたはサービス プロバイダーは、Unicode の .msg ファイルを作成する_ulFlags_パラメーターに**MAPI_UNICODE**フラグを設定する、 [OpenIMsgOnIStg](openimsgonistg.md)関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-402">A client or service provider can call the [OpenIMsgOnIStg](openimsgonistg.md) function, setting the **MAPI_UNICODE** flag in the  _ulFlags_ parameter to create Unicode .msg files.</span></span> <span data-ttu-id="45b2d-403">結果[IMessage: IMAPIProp](imessageimapiprop.md)ファイルは、 [PidTagStoreSupportMask の標準的なプロパティ](pidtagstoresupportmask-canonical-property.md)に**STORE_UNICODE_OK**を示しています、Unicode プロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-403">The resulting [IMessage : IMAPIProp](imessageimapiprop.md) file shows **STORE_UNICODE_OK** in its [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> <span data-ttu-id="45b2d-404">この定数は、mapidefs.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-404">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="45b2d-405">MDB_ONLINE</span><span class="sxs-lookup"><span data-stu-id="45b2d-405">MDB_ONLINE</span></span>  <br/> |<span data-ttu-id="45b2d-406">0x00000100</span><span class="sxs-lookup"><span data-stu-id="45b2d-406">0x00000100</span></span>  <br/> |<span data-ttu-id="45b2d-407">Outlook が Exchange キャッシュ モードの場合は、クライアントまたはサービス プロバイダー メソッドを呼び出して、 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) 、ローカル メッセージ ストアへの接続をオーバーライドし、開く_ulFlags_パラメーターで**MDB_ONLINE**フラグを設定します。リモート サーバー上のストアです。</span><span class="sxs-lookup"><span data-stu-id="45b2d-407">If Outlook is in Cached Exchange Mode, a client or service provider can call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method, setting the **MDB_ONLINE** flag in the  _ulFlags_ parameter to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="45b2d-408">開くことができない、Exchange ストアをキャッシュ モードと非キャッシュ モードで新しい MAPI セッションに同時に注意してください。</span><span class="sxs-lookup"><span data-stu-id="45b2d-408">Note that you cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="45b2d-409">キャッシュされたメッセージ ストアを既に開いている場合、このフラグで開き、またはこのフラグを使用してリモート サーバー上の Exchange ストアを開く新しい MAPI セッションを開始する前にストアを閉じる必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="45b2d-409">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>  <br/> |
|<span data-ttu-id="45b2d-410">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="45b2d-410">NON_EMS_XP_SAVE</span></span>  <br/> |<span data-ttu-id="45b2d-411">0x00001000</span><span class="sxs-lookup"><span data-stu-id="45b2d-411">0x00001000</span></span>  <br/> |<span data-ttu-id="45b2d-412">クライアントは、Exchange サーバーからメッセージが配信されていないことを示すために_ulFlags_パラメーターに**NON_EMS_XP_SAVE**フラグを設定する、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-412">A client can call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method, setting the **NON_EMS_XP_SAVE** flag in the  _ulFlags_ parameter to indicate that the message has not been delivered from an Exchange server.</span></span> <span data-ttu-id="45b2d-413">このフラグは組み合わせて使用する_ulFlags_パラメーターに**ITEMPROC_FORCE**フラグを使用してを示すメッセージが pst ファイルの前に処理ルールの対象とする PST ストアにストアに通知の到着をリッスンしているクライアントはすべて、メッセージ。</span><span class="sxs-lookup"><span data-stu-id="45b2d-413">This flag should be used in combination with the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter to indicate to a PST store that the message is eligible for rules processing before the PST store notifies any listening client of the arrival of the message.</span></span> <span data-ttu-id="45b2d-414">これは、ルールを (場合に Exchange サーバーは既に処理が、メッセージのルール)、Exchange サーバーではないサーバー上の[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)で作成された新しいメッセージに適用されますのみを処理します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-414">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange server (in which case the Exchange server would have already processed rules on the message).</span></span>  <br/> |
|<span data-ttu-id="45b2d-415">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="45b2d-415">SPAMFILTER_ONSAVE</span></span>  <br/> |<span data-ttu-id="45b2d-416">0x00000080</span><span class="sxs-lookup"><span data-stu-id="45b2d-416">0x00000080</span></span>  <br/> |<span data-ttu-id="45b2d-417">クライアントは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)、 **SPAMFILTER_ONSAVE**フラグを設定して迷惑メールが保存されるメッセージのフィルタ リングを有効にする_ulFlags_パラメーターを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-417">A client can call [IMAPIProp::SaveChanges](imapiprop-savechanges.md), setting the **SPAMFILTER_ONSAVE** flag in the  _ulFlags_ parameter to enable spam filtering on a message that is being saved.</span></span> <span data-ttu-id="45b2d-418">スパムのフィルタ リングのサポートは、送信者の電子メール アドレスの種類は、簡易メール転送プロトコル (SMTP)、メッセージは個人用フォルダー ファイル (PST) のストアに保存されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-418">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>  <br/> |
|<span data-ttu-id="45b2d-419">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="45b2d-419">STORE_ITEMPROC</span></span>  <br/> |<span data-ttu-id="45b2d-420">0x00200000</span><span class="sxs-lookup"><span data-stu-id="45b2d-420">0x00200000</span></span>  <br/> |<span data-ttu-id="45b2d-421">ラップされた PST ストアの[PidTagStoreSupportMask の標準的なプロパティ](pidtagstoresupportmask-canonical-property.md)で、このフラグが設定されている場合は、ストアでは、新しいメッセージが到着すると、ストアには、ルールを個別に、メッセージに適用されるスパムのフィルタ リングを示します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-421">If this flag is set in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) of a wrapped PST store, it indicates that when a new message arrives at the store, the store has rules and spam filtering processed on the message separately.</span></span> <span data-ttu-id="45b2d-422">ストアは、 [IMAPISupport::Notify](imapisupport-notify.md)、 **fnevNewMail**をパラメーターとして渡される[通知](notification.md)の構造体に設定し、リッスンしているクライアントに新しいメッセージの詳細を渡すことを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-422">The store then calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and passing the details of the new message to a listening client.</span></span> <span data-ttu-id="45b2d-423">その後、リッスンしているクライアントでは、通知を受信すると、メッセージのルールは処理されません。</span><span class="sxs-lookup"><span data-stu-id="45b2d-423">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span>  <br/> |
|<span data-ttu-id="45b2d-424">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="45b2d-424">STORE_UNICODE_OK</span></span>  <br/> |<span data-ttu-id="45b2d-425">0x00040000</span><span class="sxs-lookup"><span data-stu-id="45b2d-425">0x00040000</span></span>  <br/> |<span data-ttu-id="45b2d-426">[PidTagStoreSupportMask の標準的なプロパティ](pidtagstoresupportmask-canonical-property.md)には、このフラグが含まれる場合、は、ストアが Unicode のストレージをサポートしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-426">If this flag is included in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md), it indicates that the store supports Unicode storage.</span></span> <span data-ttu-id="45b2d-427">クライアントは Unicode 情報をストアに保存するかを要求するかを決定するフラグの有無を確認できます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-427">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span>  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a><span data-ttu-id="45b2d-428">フォルダー内のアイテムをアーカイブするための定義</span><span class="sxs-lookup"><span data-stu-id="45b2d-428">Definitions for archiving items in a folder</span></span>

<span data-ttu-id="45b2d-429">次の定数の定義は、 [PidTagAgingGranularity の標準的なプロパティ](pidtagaginggranularity-canonical-property.md)を設定するために使用する値です。</span><span class="sxs-lookup"><span data-stu-id="45b2d-429">The following constant definitions are values used to set the [PidTagAgingGranularity Canonical Property](pidtagaginggranularity-canonical-property.md).</span></span>
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a><span data-ttu-id="45b2d-430">リモート オブジェクトを表示するための定義</span><span class="sxs-lookup"><span data-stu-id="45b2d-430">Definitions for displaying remote objects</span></span>

<span data-ttu-id="45b2d-431">次の定数とマクロの定義は、リモート オブジェクトを表示するのには。</span><span class="sxs-lookup"><span data-stu-id="45b2d-431">The following constant and macro definitions are for displaying remote objects.</span></span> <span data-ttu-id="45b2d-432">詳細については、 [PidTagDisplayTypeEx の標準的なプロパティ](pidtagdisplaytypeex-canonical-property.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45b2d-432">For more information, see the [PidTagDisplayTypeEx Canonical Property](pidtagdisplaytypeex-canonical-property.md).</span></span>
  
```cpp
#define DTE_FLAG_REMOTE_VALID0x80000000 
#define DTE_FLAG_ACL_CAPABLE    0x40000000 
#define DTE_MASK_REMOTE        0x0000ff00 
#define DTE_MASK_LOCAL        0x000000ff 
  
#define DTE_IS_REMOTE_VALID(v)(!!((v) & DTE_FLAG_REMOTE_VALID)) 
#define DTE_IS_ACL_CAPABLE(v)(!!((v) & DTE_FLAG_ACL_CAPABLE)) 
#define DTE_REMOTE(v)(((v) & DTE_MASK_REMOTE) >> 8) 
#define DTE_LOCAL(v)((v) & DTE_MASK_LOCAL) 
  
#define DT_ROOM((ULONG) 0x00000007) 
#define DT_EQUIPMENT((ULONG) 0x00000008) 
#define DT_SEC_DISTLIST((ULONG) 0x00000009)
```

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a><span data-ttu-id="45b2d-433">エラー コードを格納する Exchange のアドレス帳とメッセージの定義</span><span class="sxs-lookup"><span data-stu-id="45b2d-433">Definitions for Exchange address book and Message store error codes</span></span>

<span data-ttu-id="45b2d-434">次には、再接続の機能が搭載されている Exchange のアドレス帳とメッセージ ・ ストアのエラー コード定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-434">The following contains error code definitions for the Exchange Address Book and Message Store, which have reconnection capability.</span></span> <span data-ttu-id="45b2d-435">最後の呼び出しの切断されたグローバル カタログ (GC) に**MAPI_E_END_OF_SESSION**エラーを再試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45b2d-435">The last call to a disconnected Global Catalog (GC) may result in the **MAPI_E_END_OF_SESSION** error, which would need to be retried.</span></span> 
  
<span data-ttu-id="45b2d-436">Outlook の MAPI サポートへの再接続 GC サーバーに特別な再構成がその他のエラー コードをクライアントに返すことができます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-436">Outlook's MAPI supports reconnection to a GC server without special reconfiguration, but some other error codes can be returned to the client.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="45b2d-437">MAPI_E_END_OF_SESSION</span><span class="sxs-lookup"><span data-stu-id="45b2d-437">MAPI_E_END_OF_SESSION</span></span>  <br/> |<span data-ttu-id="45b2d-438">0x80040200</span><span class="sxs-lookup"><span data-stu-id="45b2d-438">0x80040200</span></span>  <br/> |<span data-ttu-id="45b2d-439">接続が切断されたときに返されます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-439">Returned when a connection has been disconnected.</span></span>  <br/> |
|<span data-ttu-id="45b2d-440">MAPI_E_RECONNECTED</span><span class="sxs-lookup"><span data-stu-id="45b2d-440">MAPI_E_RECONNECTED</span></span>  <br/> |<span data-ttu-id="45b2d-441">0x80040125</span><span class="sxs-lookup"><span data-stu-id="45b2d-441">0x80040125</span></span>  <br/> |<span data-ttu-id="45b2d-442">リモート プロシージャ コール (RPC) 接続のトークンが最新でない場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-442">Returned when the Remote Procedure Call (RPC) connection token is out-of-date.</span></span> <span data-ttu-id="45b2d-443">現在のトランザクションのトークンとは異なる場合ことを意味する接続のトークンが再接続、 **MAPI_E_RECONNECTED**が返されすることができますので**MAPI_E_END_OF_SESSION**と同じに扱われます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-443">If the token of the current transaction is different from the token of the connection that means it has reconnected, so **MAPI_E_RECONNECTED** is returned and can be treated the same as **MAPI_E_END_OF_SESSION**.</span></span> <span data-ttu-id="45b2d-444">呼び出しを再試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45b2d-444">The call should be retried.</span></span>  <br/> |
|<span data-ttu-id="45b2d-445">MAPI_E_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="45b2d-445">MAPI_E_OFFLINE</span></span>  <br/> |<span data-ttu-id="45b2d-446">0x80040126</span><span class="sxs-lookup"><span data-stu-id="45b2d-446">0x80040126</span></span>  <br/> |<span data-ttu-id="45b2d-447">接続がオフラインのときに返されます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-447">Returned when the connection is offline.</span></span> <span data-ttu-id="45b2d-448">つまり、通常サーバーの障害またはネットワーク接続が失われるなど、環境に何かが発生したことです。</span><span class="sxs-lookup"><span data-stu-id="45b2d-448">Typically this means that something has occurred in the environment, such as server failure or loss of network connectivity.</span></span> <span data-ttu-id="45b2d-449">このエラーは、キャッシュ モードを使用する場合に発生する可能性があります、プロファイル、およびサーバーと通信するためにキャッシュをバイパスしようとしています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-449">This error is most likely to occur when using a cached mode profile and attempting to bypass the cache to communicate with the server.</span></span> <span data-ttu-id="45b2d-450">キャッシュは最初にサーバーへの接続を確立することはありませんでした、 **MAPI_E_OFFLINE**の表面に使用可能性があります、オフライン状態である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="45b2d-450">If the cache was never able to initially establish a connection to the server, it may be in the offline state in which **MAPI_E_OFFLINE** could surface.</span></span>  <br/> |
   
<span data-ttu-id="45b2d-451">上記の 2 つのエラーのどちらも表示されますすべてのシナリオで表示される場所は多くの場合を適用します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-451">Neither of the preceding two errors will be returned in all scenarios where they would likely appear to apply.</span></span> <span data-ttu-id="45b2d-452">ほとんどの場合、 **MAPI\_E_NETWORK_ERROR** **MAPI_E_CALL_FAILED**が返されますか。</span><span class="sxs-lookup"><span data-stu-id="45b2d-452">In most cases, **MAPI\_E_NETWORK_ERROR** or **MAPI_E_CALL_FAILED** will be returned.</span></span> <span data-ttu-id="45b2d-453">[MAPI クライアントの Microsoft Exchange Server と共同作業データ オブジェクト 1.2.1](http://support.microsoft.com/kb/171440)のダウンロードを使用しても表示されます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-453">Neither will appear using the [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) download.</span></span> 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a><span data-ttu-id="45b2d-454">Exchange Server メールボックスの定義がキャッシュ モードのクォータ</span><span class="sxs-lookup"><span data-stu-id="45b2d-454">Definitions for Exchange Server Mailbox cached mode quotas</span></span>

<span data-ttu-id="45b2d-455">次の定数の定義は、Microsoft Outlook 2010 で使用され、Exchange を設定するのには、Microsoft Outlook 2013 のキャッシュ モード プロファイル クォータは、それ以外の場合、オンライン プロファイルでのみ使用可能な Exchange メールボックスのクォータに相当します。</span><span class="sxs-lookup"><span data-stu-id="45b2d-455">The following constant definitions are used by Microsoft Outlook 2010 and Microsoft Outlook 2013 to set the Exchange cached mode profile quotas that are equivalent to the Exchange mailbox quotas otherwise available only with an online profile.</span></span>
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

<span data-ttu-id="45b2d-456">これらのプロパティは、通信のオンラインのプロパティにマップされ、キロバイト単位で同じ値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="45b2d-456">These properties map to their correspondent online properties and contain the same values in kilobytes.</span></span> <span data-ttu-id="45b2d-457">PR_QUOTA_WARNING は、PR_STORAGE_QUOTA_LIMIT へ PR_QUOTA_PROHIBIT_SEND_QUOTA、PR_QUOTA_SEND と PR_PROHIBIT_RECEIVE_QUOTA を PR_QUOTA_RECEIVE にマップされます。</span><span class="sxs-lookup"><span data-stu-id="45b2d-457">PR_QUOTA_WARNING maps to PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND to PR_QUOTA_PROHIBIT_SEND_QUOTA, and PR_QUOTA_RECEIVE to PR_PROHIBIT_RECEIVE_QUOTA.</span></span>
  
### <a name="definitions-for-message-format"></a><span data-ttu-id="45b2d-458">メッセージ形式の定義</span><span class="sxs-lookup"><span data-stu-id="45b2d-458">Definitions for message format</span></span>

<span data-ttu-id="45b2d-459">次の定数の定義は、 [PidTagMessageEditorFormat の標準的なプロパティ](pidtagmessageeditorformat-canonical-property.md)を設定するために使用する値です。</span><span class="sxs-lookup"><span data-stu-id="45b2d-459">The following constant definitions are values that are used to set the [PidTagMessageEditorFormat Canonical Property](pidtagmessageeditorformat-canonical-property.md).</span></span>
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a><span data-ttu-id="45b2d-460">HTTP 経由で RPC を使用するための定義</span><span class="sxs-lookup"><span data-stu-id="45b2d-460">Definitions for using RPC over HTTP</span></span>

<span data-ttu-id="45b2d-461">プロパティを設定するのにはフラグとして使用される定数の定義は[PidTagRpcOverHttpFlags の標準的なプロパティ](pidtagrpcoverhttpflags-canonical-property.md)のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="45b2d-461">See the [PidTagRpcOverHttpFlags Canonical Property](pidtagrpcoverhttpflags-canonical-property.md) topic for constant definitions used as flags to set the property.</span></span> 
  
<span data-ttu-id="45b2d-462">プロパティを設定するために使用する定数の定義は[PidTagRpcOverHttpProxyAuthScheme の標準的なプロパティ](pidtagrpcoverhttpproxyauthscheme-canonical-property.md)のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="45b2d-462">See the [PidTagRpcOverHttpProxyAuthScheme Canonical Property](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) topic for constant definitions used to set the property.</span></span> 
  
### <a name="identifiers"></a><span data-ttu-id="45b2d-463">識別子</span><span class="sxs-lookup"><span data-stu-id="45b2d-463">Identifiers</span></span>

<span data-ttu-id="45b2d-464">使用して、`DEFINE_OLEGUID`の値は次の GUID のシンボリック名を関連付けるには Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル guiddef.h に定義されているマクロ。</span><span class="sxs-lookup"><span data-stu-id="45b2d-464">Use the  `DEFINE_OLEGUID` macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the following GUID symbolic names with their values.</span></span> 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

<span data-ttu-id="45b2d-465">次の識別子は、複数の ([MultiEx](using-multiple-exchange-accounts.md)) の Exchange メールボックスをサポートするためを効果的に既定値を無効にする[PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)プロパティが含まれているアドレス帳の Capone プロファイル セクションのします。[SetDefaultDir](iaddrbook-setdefaultdir.md)で指定されたコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="45b2d-465">The following Identifier is for the Capone Profile section of an Address Book, which in support of multiple Exchange ([MultiEx](using-multiple-exchange-accounts.md)) mailboxes contains a [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property that effectively turns off the default container specified by [SetDefaultDir](iaddrbook-setdefaultdir.md).</span></span>
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a><span data-ttu-id="45b2d-466">インターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="45b2d-466">Interface identifiers</span></span>

#### <a name="imapisync"></a><span data-ttu-id="45b2d-467">IMAPISync</span><span class="sxs-lookup"><span data-stu-id="45b2d-467">IMAPISync</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a><span data-ttu-id="45b2d-468">IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="45b2d-468">IMAPISyncProgressCallback</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a><span data-ttu-id="45b2d-469">IID_IContabAdmin</span><span class="sxs-lookup"><span data-stu-id="45b2d-469">IID_IContabAdmin</span></span>
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a><span data-ttu-id="45b2d-470">IID_IMAPISECUREMESSAGE</span><span class="sxs-lookup"><span data-stu-id="45b2d-470">IID_IMAPISECUREMESSAGE</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a><span data-ttu-id="45b2d-471">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="45b2d-471">IID_IMAPIGetSession</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a><span data-ttu-id="45b2d-472">PST のオーバーライドのハンドラーのインターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="45b2d-472">PST Override Handler interface identifiers</span></span>

#### <a name="iidipstoverridereq"></a><span data-ttu-id="45b2d-473">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="45b2d-473">IID_IPSTOVERRIDEREQ</span></span>
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a><span data-ttu-id="45b2d-474">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="45b2d-474">IID_IPSTOVERRIDE1</span></span>
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a><span data-ttu-id="45b2d-475">関連項目</span><span class="sxs-lookup"><span data-stu-id="45b2d-475">See also</span></span>

- [<span data-ttu-id="45b2d-476">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="45b2d-476">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="45b2d-477">Outlook で使用される名前付きプロパティについて</span><span class="sxs-lookup"><span data-stu-id="45b2d-477">About Named Properties Used by Outlook</span></span>](about-named-properties-used-by-outlook.md)
- [<span data-ttu-id="45b2d-478">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする</span><span class="sxs-lookup"><span data-stu-id="45b2d-478">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="45b2d-479">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く</span><span class="sxs-lookup"><span data-stu-id="45b2d-479">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="45b2d-480">Exchange キャッシュ モードで同期を呼び出すことなく OST でメッセージを管理する</span><span class="sxs-lookup"><span data-stu-id="45b2d-480">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

