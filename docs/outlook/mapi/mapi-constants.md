---
title: MAPI 定数
manager: soliver
ms.date: 10/02/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: MAPI API で使用する定数の定義、MAPI インターフェイス宣言、クラスとインターフェイス識別子。
ms.openlocfilehash: 343b777550d88276a1f5cad19f12ae7fc09c6244
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393734"
---
# <a name="mapi-constants"></a><span data-ttu-id="72457-103">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="72457-103">MAPI Constants</span></span>

<span data-ttu-id="72457-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72457-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72457-105">このトピックでは、MAPI API で使用する定数の定義、MAPI インターフェイス宣言、クラスとインターフェイス識別子について説明します。</span><span class="sxs-lookup"><span data-stu-id="72457-105">This topic contains constant definitions, MAPI interface declarations, and class and interface identifiers used by the MAPI APIs.</span></span>
  
## <a name="class-and-interface-identifiers"></a><span data-ttu-id="72457-106">クラスとインターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="72457-106">Class and interface identifiers</span></span>

<span data-ttu-id="72457-107">他の指定がなければ、Microsoft Windows ソフトウェア開発キット (SDK) の guiddef.h ヘッダー ファイルで定義されている DEFINE_GUID マクロを使用して、グローバル一意識別子 (GUID) のシンボリック名とその値を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="72457-107">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values, unless otherwise indicated.</span></span>
  
## <a name="attachment-security-conversion-api"></a><span data-ttu-id="72457-108">添付ファイル セキュリティ変換 API</span><span class="sxs-lookup"><span data-stu-id="72457-108">Attachment security conversion API</span></span>

<span data-ttu-id="72457-109">このセクションでは、添付ファイル セキュリティ API に関する定数の定義とインターフェイス識別子について説明します。</span><span class="sxs-lookup"><span data-stu-id="72457-109">This section contains constant definitions and interface identifiers for the Attachment Security API.</span></span>
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

<span data-ttu-id="72457-110">純粋仮想関数 **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)** を定義するには、Windows SDK の mapidefs.h ヘッダー ファイルで定義されている MAPIMETHOD マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="72457-110">Use the MAPIMETHOD macro defined in the Windows SDK header file mapidefs.h to define the pure virtual function **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span></span> 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

<span data-ttu-id="72457-111">**[IAttachmentSecurity](iattachmentsecurityiunknown.md)** の仮想メソッド テーブルを定義するには、Windows SDK の mapidefs.h ヘッダー ファイルで定義されている DECLARE_MAPI_INTERFACE_ マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="72457-111">Use the DECLARE_MAPI_INTERFACE_ macro defined in the Windows SDK header file mapidefs.h to define the virtual method table for **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span></span> 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a><span data-ttu-id="72457-112">MAPI-MIME 会話 API</span><span class="sxs-lookup"><span data-stu-id="72457-112">MAPI-MIME conversion API</span></span>

<span data-ttu-id="72457-113">このセクションでは、MAPI-MIME 会話 API に関する定数の定義、クラスとインターフェイス識別子について説明します。</span><span class="sxs-lookup"><span data-stu-id="72457-113">This section contains constant definitions and class and interface identifiers for the MAPI-MIME Conversion API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="72457-114">定数</span><span class="sxs-lookup"><span data-stu-id="72457-114">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72457-115">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="72457-115">CCSF_SMTP</span></span>  <br/> |<span data-ttu-id="72457-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="72457-116">0x0002</span></span>  <br/> |
|<span data-ttu-id="72457-117">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="72457-117">CCSF_NOHEADERS</span></span>  <br/> |<span data-ttu-id="72457-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="72457-118">0x0004</span></span>  <br/> |
|<span data-ttu-id="72457-119">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="72457-119">CCSF_USE_TNEF</span></span>  <br/> | <span data-ttu-id="72457-120">0x0010</span><span class="sxs-lookup"><span data-stu-id="72457-120">0x0010</span></span>  <br/> |
|<span data-ttu-id="72457-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="72457-121">CCSF_INCLUDE_BCC</span></span>  <br/> |<span data-ttu-id="72457-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="72457-122">0x0020</span></span>  <br/> |
|<span data-ttu-id="72457-123">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="72457-123">CCSF_8BITHEADERS</span></span>  <br/> | <span data-ttu-id="72457-124">0x0040</span><span class="sxs-lookup"><span data-stu-id="72457-124">0x0040</span></span>  <br/> |
|<span data-ttu-id="72457-125">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="72457-125">CCSF_USE_RTF</span></span>  <br/> |<span data-ttu-id="72457-126">0x0080</span><span class="sxs-lookup"><span data-stu-id="72457-126">0x0080</span></span>  <br/> |
|<span data-ttu-id="72457-127">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="72457-127">CCSF_PLAIN_TEXT_ONLY</span></span>  <br/> |<span data-ttu-id="72457-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="72457-128">0x1000</span></span>  <br/> |
|<span data-ttu-id="72457-129">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="72457-129">CCSF_NO_MSGID</span></span>  <br/> |<span data-ttu-id="72457-130">0x4000</span><span class="sxs-lookup"><span data-stu-id="72457-130">0x4000</span></span>  <br/> |
|<span data-ttu-id="72457-131">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="72457-131">CCSF_GLOBAL_MESSAGE</span></span>  <br/> |<span data-ttu-id="72457-132">0x00200000</span><span class="sxs-lookup"><span data-stu-id="72457-132">0x00200000</span></span>  <br/> |
|<span data-ttu-id="72457-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="72457-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="72457-134">*Microsoft Windows ソフトウェア開発キット (SDK) の winerror.h ヘッダーファイルで定義されています*</span><span class="sxs-lookup"><span data-stu-id="72457-134">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="72457-135">クラス識別子</span><span class="sxs-lookup"><span data-stu-id="72457-135">Class identifiers</span></span>

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a><span data-ttu-id="72457-136">インターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="72457-136">Interface identifiers</span></span>

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a><span data-ttu-id="72457-137">オフライン状態 API</span><span class="sxs-lookup"><span data-stu-id="72457-137">About the Offline State API</span></span>

<span data-ttu-id="72457-138">このセクションでは、オフライン状態 API に関する定数の定義、クラスとインターフェイス識別子について説明します。</span><span class="sxs-lookup"><span data-stu-id="72457-138">This section contains constant definitions and class and interface identifiers for the Offline State API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="72457-139">定数</span><span class="sxs-lookup"><span data-stu-id="72457-139">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72457-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="72457-140">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="72457-141">*Microsoft Windows ソフトウェア開発キット (SDK) の winerror.h ヘッダーファイルで定義されています*</span><span class="sxs-lookup"><span data-stu-id="72457-141">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="72457-142">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="72457-142">E_NOINTERFACE</span></span>  <br/> | <span data-ttu-id="72457-143">*Windows (SDK) の winerror.h ヘッダー ファイルで定義されています*</span><span class="sxs-lookup"><span data-stu-id="72457-143">*As defined in the Windows (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="72457-144">MAPIOFFLINE_ADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="72457-144">MAPIOFFLINE_ADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="72457-145">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="72457-145">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="72457-146">MAPIOFFLINE_UNADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="72457-146">MAPIOFFLINE_UNADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="72457-147">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="72457-147">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="72457-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="72457-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span></span>  <br/> |<span data-ttu-id="72457-149">1</span><span class="sxs-lookup"><span data-stu-id="72457-149">-1</span></span>  <br/> |
|<span data-ttu-id="72457-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="72457-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="72457-151">0x1</span><span class="sxs-lookup"><span data-stu-id="72457-151">0x1</span></span>  <br/> |
|<span data-ttu-id="72457-152">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="72457-152">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="72457-153">0x2</span><span class="sxs-lookup"><span data-stu-id="72457-153">0x2</span></span>  <br/> |
|<span data-ttu-id="72457-154">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="72457-154">MAPIOFFLINE_FLAG_BLOCK</span></span>  <br/> |<span data-ttu-id="72457-155">0x00002000</span><span class="sxs-lookup"><span data-stu-id="72457-155">0x00002000</span></span>  <br/> |
|<span data-ttu-id="72457-156">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="72457-156">MAPIOFFLINE_FLAG_DEFAULT</span></span>  <br/> |<span data-ttu-id="72457-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72457-157">0x00000000</span></span>  <br/> |
|<span data-ttu-id="72457-158">MAPIOFFLINE_STATE_ALL</span><span class="sxs-lookup"><span data-stu-id="72457-158">MAPIOFFLINE_STATE_ALL</span></span>  <br/> |<span data-ttu-id="72457-159">0x003f037f</span><span class="sxs-lookup"><span data-stu-id="72457-159">0x003f037f</span></span>  <br/> |
|<span data-ttu-id="72457-160">**オンラインまたはオフライン**</span><span class="sxs-lookup"><span data-stu-id="72457-160">**Online or offline**</span></span> <br/> ||
|<span data-ttu-id="72457-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span><span class="sxs-lookup"><span data-stu-id="72457-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span></span>  <br/> |<span data-ttu-id="72457-162">0x00000003</span><span class="sxs-lookup"><span data-stu-id="72457-162">0x00000003</span></span>  <br/> |
|<span data-ttu-id="72457-163">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="72457-163">MAPIOFFLINE_STATE_OFFLINE</span></span>  <br/> |<span data-ttu-id="72457-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72457-164">0x00000001</span></span>  <br/> |
|<span data-ttu-id="72457-165">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="72457-165">MAPIOFFLINE_STATE_ONLINE</span></span>  <br/> |<span data-ttu-id="72457-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="72457-166">0x00000002</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="72457-167">クラス識別子</span><span class="sxs-lookup"><span data-stu-id="72457-167">Class identifiers</span></span>

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a><span data-ttu-id="72457-168">インターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="72457-168">Interface identifiers</span></span>

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

## <a name="outlook-named-properties"></a><span data-ttu-id="72457-169">Outlook の名前付きプロパティ</span><span class="sxs-lookup"><span data-stu-id="72457-169">Outlook named properties</span></span>

<span data-ttu-id="72457-170">このセクションでは、名前付きプロパティとその名前空間に関する定数の定義、および関連する他の定数について説明します。</span><span class="sxs-lookup"><span data-stu-id="72457-170">This section contains constant definitions for named properties and their namespaces, and other related constants.</span></span>
  
### <a name="definitions-for-named-properties"></a><span data-ttu-id="72457-171">名前付きプロパティの定義</span><span class="sxs-lookup"><span data-stu-id="72457-171">Definitions for named properties</span></span>

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

### <a name="definitions-for-namespaces"></a><span data-ttu-id="72457-172">名前空間の定義</span><span class="sxs-lookup"><span data-stu-id="72457-172">Definitions for namespaces</span></span>

<span data-ttu-id="72457-173">次のグローバル一意識別子 (GUID) は、名前付きプロパティの名前空間を表しています。</span><span class="sxs-lookup"><span data-stu-id="72457-173">The following globally unique identifiers (GUIDs) represent the namespaces of the named properties.</span></span>
  
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

<span data-ttu-id="72457-174">PSETID の定義については、MAPI ストアのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72457-174">Refer to the section MAPI Store for the PSETID definitions.</span></span>
  
### <a name="other-constants"></a><span data-ttu-id="72457-175">その他の定数</span><span class="sxs-lookup"><span data-stu-id="72457-175">Other constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72457-176">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="72457-176">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="72457-177">0xD000000</span><span class="sxs-lookup"><span data-stu-id="72457-177">0xD000000</span></span>  <br/> |
|<span data-ttu-id="72457-178">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="72457-178">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="72457-179">0x2000000</span><span class="sxs-lookup"><span data-stu-id="72457-179">0x2000000</span></span>  <br/> |
|<span data-ttu-id="72457-180">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="72457-180">MNID_ID</span></span>  <br/> | <span data-ttu-id="72457-181">*mapidefs.h ヘッダー ファイルで定義されています。*</span><span class="sxs-lookup"><span data-stu-id="72457-181">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="72457-182">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="72457-182">MNID_STRING</span></span>  <br/> | <span data-ttu-id="72457-183">*mapidefs.h ヘッダー ファイルで定義されています。*</span><span class="sxs-lookup"><span data-stu-id="72457-183">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="72457-184">mtgNone</span><span class="sxs-lookup"><span data-stu-id="72457-184">mtgNone</span></span>  <br/> |<span data-ttu-id="72457-185">0x0</span><span class="sxs-lookup"><span data-stu-id="72457-185">0x0</span></span>  <br/> |
|<span data-ttu-id="72457-186">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="72457-186">mtgRequest</span></span>  <br/> |<span data-ttu-id="72457-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72457-187">0x00000001</span></span>  <br/> |
|<span data-ttu-id="72457-188">mtgFullUpdate</span><span class="sxs-lookup"><span data-stu-id="72457-188">mtgFullUpdate</span></span>  <br/> |<span data-ttu-id="72457-189">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-189">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-190">mtgInfoUpdate</span><span class="sxs-lookup"><span data-stu-id="72457-190">mtgInfoUpdate</span></span>  <br/> |<span data-ttu-id="72457-191">0x00020000</span><span class="sxs-lookup"><span data-stu-id="72457-191">0x00020000</span></span>  <br/> |
|<span data-ttu-id="72457-192">mtgOutofDate</span><span class="sxs-lookup"><span data-stu-id="72457-192">mtgOutofDate</span></span>  <br/> |<span data-ttu-id="72457-193">0x00080000</span><span class="sxs-lookup"><span data-stu-id="72457-193">0x00080000</span></span>  <br/> |
|<span data-ttu-id="72457-194">mtgDelegated</span><span class="sxs-lookup"><span data-stu-id="72457-194">mtgDelegated</span></span>  <br/> |<span data-ttu-id="72457-195">0x00100000</span><span class="sxs-lookup"><span data-stu-id="72457-195">0x00100000</span></span>  <br/> |
   
## <a name="replication-api"></a><span data-ttu-id="72457-196">レプリケーション API</span><span class="sxs-lookup"><span data-stu-id="72457-196">About the Replication API</span></span>

<span data-ttu-id="72457-197">このセクションでは、レプリケーション API に関する定数の定義、MAPI インターフェイス宣言、クラスとインターフェイス識別子について説明します。</span><span class="sxs-lookup"><span data-stu-id="72457-197">This section contains constant definitions, MAPI interface declarations, and class and interface identifiers for the Replication API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="72457-198">定数</span><span class="sxs-lookup"><span data-stu-id="72457-198">Constants</span></span>

<span data-ttu-id="72457-199">以下は、MAPI サービス プロバイダーを特定する [MAPIUID](mapiuid.md) 構造です。</span><span class="sxs-lookup"><span data-stu-id="72457-199">The following is a [MAPIUID](mapiuid.md) structure identifying a MAPI service provider:</span></span> 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|<span data-ttu-id="72457-200">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="72457-200">DNH_OK</span></span>  <br/> |<span data-ttu-id="72457-201">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-201">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-202">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="72457-202">DNT_OK</span></span>  <br/> |<span data-ttu-id="72457-203">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-203">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-204">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="72457-204">HSF_LOCAL</span></span>  <br/> |<span data-ttu-id="72457-205">0x00000008</span><span class="sxs-lookup"><span data-stu-id="72457-205">0x00000008</span></span>  <br/> |
|<span data-ttu-id="72457-206">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="72457-206">HSF_COPYDESTRUCTIVE</span></span>  <br/> |<span data-ttu-id="72457-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72457-207">0x00000010</span></span>  <br/> |
|<span data-ttu-id="72457-208">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="72457-208">HSF_OK</span></span>  <br/> |<span data-ttu-id="72457-209">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-209">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-210">MDB_OST_LOGON_UNICODE</span><span class="sxs-lookup"><span data-stu-id="72457-210">MDB_OST_LOGON_UNICODE</span></span>  <br/> |<span data-ttu-id="72457-211">((ULONG) 0x00000800)</span><span class="sxs-lookup"><span data-stu-id="72457-211">((ULONG) 0x00000800)</span></span>  <br/> |
|<span data-ttu-id="72457-212">MDB_OST_LOGON_ANSI</span><span class="sxs-lookup"><span data-stu-id="72457-212">MDB_OST_LOGON_ANSI</span></span>  <br/> |<span data-ttu-id="72457-213">((ULONG) 0x00001000)</span><span class="sxs-lookup"><span data-stu-id="72457-213">((ULONG) 0x00001000)</span></span>  <br/> |
|<span data-ttu-id="72457-214">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="72457-214">SHOW_SOFT_DELETES</span></span>  <br/> |<span data-ttu-id="72457-215">((ULONG) 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="72457-215">((ULONG) 0x00000002)</span></span>  <br/> |
|<span data-ttu-id="72457-216">SS_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="72457-216">SS_ACTIVE</span></span>  <br/> |<span data-ttu-id="72457-217">0</span><span class="sxs-lookup"><span data-stu-id="72457-217">{0}</span></span>  <br/> |
|<span data-ttu-id="72457-218">SS_SUSPENDED</span><span class="sxs-lookup"><span data-stu-id="72457-218">SS_SUSPENDED</span></span>  <br/> |<span data-ttu-id="72457-219">1</span><span class="sxs-lookup"><span data-stu-id="72457-219">-1</span></span>  <br/> |
|<span data-ttu-id="72457-220">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="72457-220">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="72457-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72457-221">0x00000001</span></span>  <br/> |
|<span data-ttu-id="72457-222">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="72457-222">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="72457-223">0x00000002</span><span class="sxs-lookup"><span data-stu-id="72457-223">0x00000002</span></span>  <br/> |
|<span data-ttu-id="72457-224">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="72457-224">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="72457-225">0x00000040</span><span class="sxs-lookup"><span data-stu-id="72457-225">0x00000040</span></span>  <br/> |
|<span data-ttu-id="72457-226">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="72457-226">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="72457-227">0x00000080</span><span class="sxs-lookup"><span data-stu-id="72457-227">0x00000080</span></span>  <br/> |
|<span data-ttu-id="72457-228">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="72457-228">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="72457-229">0x00000200</span><span class="sxs-lookup"><span data-stu-id="72457-229">0x00000200</span></span>  <br/> |
|<span data-ttu-id="72457-230">SYNC_BACKGROUND</span><span class="sxs-lookup"><span data-stu-id="72457-230">SYNC_BACKGROUND</span></span>  <br/> |<span data-ttu-id="72457-231">0x00001000</span><span class="sxs-lookup"><span data-stu-id="72457-231">0x00001000</span></span>  <br/> |
|<span data-ttu-id="72457-232">SYNC_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="72457-232">SYNC_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="72457-233">0x00020000</span><span class="sxs-lookup"><span data-stu-id="72457-233">0x00020000</span></span>  <br/> |
|<span data-ttu-id="72457-234">SYNC_HEADERS</span><span class="sxs-lookup"><span data-stu-id="72457-234">SYNC_HEADERS</span></span>  <br/> |<span data-ttu-id="72457-235">0x02000000</span><span class="sxs-lookup"><span data-stu-id="72457-235">0x02000000</span></span>  <br/> |
|<span data-ttu-id="72457-236">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="72457-236">UPC_OK</span></span>  <br/> |<span data-ttu-id="72457-237">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-237">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-238">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="72457-238">UPD_ASSOC</span></span>  <br/> |<span data-ttu-id="72457-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72457-239">0x00000001</span></span>  <br/> |
|<span data-ttu-id="72457-240">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="72457-240">UPD_MOV</span></span>  <br/> |<span data-ttu-id="72457-241">0x00000002</span><span class="sxs-lookup"><span data-stu-id="72457-241">0x00000002</span></span>  <br/> |
|<span data-ttu-id="72457-242">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="72457-242">UPD_OK</span></span>  <br/> |<span data-ttu-id="72457-243">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-243">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-244">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="72457-244">UPD_MOVED</span></span>  <br/> |<span data-ttu-id="72457-245">0x00020000</span><span class="sxs-lookup"><span data-stu-id="72457-245">0x00020000</span></span>  <br/> |
|<span data-ttu-id="72457-246">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="72457-246">UPD_UPDATE</span></span>  <br/> |<span data-ttu-id="72457-247">0x00040000</span><span class="sxs-lookup"><span data-stu-id="72457-247">0x00040000</span></span>  <br/> |
|<span data-ttu-id="72457-248">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="72457-248">UPD_COMMIT</span></span>  <br/> |<span data-ttu-id="72457-249">0x00080000</span><span class="sxs-lookup"><span data-stu-id="72457-249">0x00080000</span></span>  <br/> |
|<span data-ttu-id="72457-250">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="72457-250">UPF_NEW</span></span>  <br/> |<span data-ttu-id="72457-251">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72457-251">0x00000001</span></span>  <br/> |
|<span data-ttu-id="72457-252">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="72457-252">UPF_MOD_PARENT</span></span>  <br/> |<span data-ttu-id="72457-253">0x00000002</span><span class="sxs-lookup"><span data-stu-id="72457-253">0x00000002</span></span>  <br/> |
|<span data-ttu-id="72457-254">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="72457-254">UPF_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="72457-255">0x00000004</span><span class="sxs-lookup"><span data-stu-id="72457-255">0x00000004</span></span>  <br/> |
|<span data-ttu-id="72457-256">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="72457-256">UPF_DEL</span></span>  <br/> |<span data-ttu-id="72457-257">0x00000008</span><span class="sxs-lookup"><span data-stu-id="72457-257">0x00000008</span></span>  <br/> |
|<span data-ttu-id="72457-258">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="72457-258">UPF_OK</span></span>  <br/> |<span data-ttu-id="72457-259">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-259">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-260">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="72457-260">UPH_OK</span></span>  <br/> |<span data-ttu-id="72457-261">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-261">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-262">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="72457-262">UPM_ASSOC</span></span>  <br/> |<span data-ttu-id="72457-263">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72457-263">0x00000001</span></span>  <br/> |
|<span data-ttu-id="72457-264">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="72457-264">UPM_NEW</span></span>  <br/> |<span data-ttu-id="72457-265">0x00000002</span><span class="sxs-lookup"><span data-stu-id="72457-265">0x00000002</span></span>  <br/> |
|<span data-ttu-id="72457-266">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="72457-266">UPM_MOV</span></span>  <br/> |<span data-ttu-id="72457-267">0x00000004</span><span class="sxs-lookup"><span data-stu-id="72457-267">0x00000004</span></span>  <br/> |
|<span data-ttu-id="72457-268">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="72457-268">UPM_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="72457-269">0x00000008</span><span class="sxs-lookup"><span data-stu-id="72457-269">0x00000008</span></span>  <br/> |
|<span data-ttu-id="72457-270">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="72457-270">UPM_HEADER</span></span>  <br/> |<span data-ttu-id="72457-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72457-271">0x00000010</span></span>  <br/> |
|<span data-ttu-id="72457-272">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="72457-272">UPM_OK</span></span>  <br/> |<span data-ttu-id="72457-273">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-273">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-274">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="72457-274">UPM_MOVED</span></span>  <br/> |<span data-ttu-id="72457-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="72457-275">0x00020000</span></span>  <br/> |
|<span data-ttu-id="72457-276">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="72457-276">UPM_COMMIT</span></span>  <br/> |<span data-ttu-id="72457-277">0x00040000</span><span class="sxs-lookup"><span data-stu-id="72457-277">0x00040000</span></span>  <br/> |
|<span data-ttu-id="72457-278">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="72457-278">UPM_DELETE</span></span>  <br/> |<span data-ttu-id="72457-279">0x00080000</span><span class="sxs-lookup"><span data-stu-id="72457-279">0x00080000</span></span>  <br/> |
|<span data-ttu-id="72457-280">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="72457-280">UPM_SAVE</span></span>  <br/> |<span data-ttu-id="72457-281">0x00100000</span><span class="sxs-lookup"><span data-stu-id="72457-281">0x00100000</span></span>  <br/> |
|<span data-ttu-id="72457-282">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="72457-282">UPR_ASSOC</span></span>  <br/> |<span data-ttu-id="72457-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72457-283">0x00000001</span></span>  <br/> |
|<span data-ttu-id="72457-284">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="72457-284">UPR_READ</span></span>  <br/> |<span data-ttu-id="72457-285">0x00000002</span><span class="sxs-lookup"><span data-stu-id="72457-285">0x00000002</span></span>  <br/> |
|<span data-ttu-id="72457-286">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="72457-286">UPR_OK</span></span>  <br/> |<span data-ttu-id="72457-287">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-287">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-288">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="72457-288">UPR_COMMIT</span></span>  <br/> |<span data-ttu-id="72457-289">0x00020000</span><span class="sxs-lookup"><span data-stu-id="72457-289">0x00020000</span></span>  <br/> |
|<span data-ttu-id="72457-290">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="72457-290">UPS_UPLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="72457-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72457-291">0x00000001</span></span>  <br/> |
|<span data-ttu-id="72457-292">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="72457-292">UPS_DNLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="72457-293">0x00000002</span><span class="sxs-lookup"><span data-stu-id="72457-293">0x00000002</span></span>  <br/> |
|<span data-ttu-id="72457-294">UPS_ONE_FOLDER</span><span class="sxs-lookup"><span data-stu-id="72457-294">UPS_ONE_FOLDER</span></span>  <br/> |<span data-ttu-id="72457-295">0x00000004</span><span class="sxs-lookup"><span data-stu-id="72457-295">0x00000004</span></span>  <br/> |
|<span data-ttu-id="72457-296">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="72457-296">UPS_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="72457-297">0x00000080</span><span class="sxs-lookup"><span data-stu-id="72457-297">0x00000080</span></span>  <br/> |
|<span data-ttu-id="72457-298">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="72457-298">UPS_OK</span></span>  <br/> |<span data-ttu-id="72457-299">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-299">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-300">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="72457-300">UPT_OK</span></span>  <br/> |<span data-ttu-id="72457-301">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-301">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-302">UPT_PUBLIC</span><span class="sxs-lookup"><span data-stu-id="72457-302">UPT_PUBLIC</span></span>  <br/> |<span data-ttu-id="72457-303">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72457-303">0x00000001</span></span>  <br/> |
|<span data-ttu-id="72457-304">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="72457-304">UPV_ERROR</span></span>  <br/> |<span data-ttu-id="72457-305">0x00010000</span><span class="sxs-lookup"><span data-stu-id="72457-305">0x00010000</span></span>  <br/> |
|<span data-ttu-id="72457-306">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="72457-306">UPV_DIRTY</span></span>  <br/> |<span data-ttu-id="72457-307">0x00020000</span><span class="sxs-lookup"><span data-stu-id="72457-307">0x00020000</span></span>  <br/> |
|<span data-ttu-id="72457-308">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="72457-308">UPV_COMMIT</span></span>  <br/> |<span data-ttu-id="72457-309">0x00040000</span><span class="sxs-lookup"><span data-stu-id="72457-309">0x00040000</span></span>  <br/> |
   
### <a name="interface-declarations"></a><span data-ttu-id="72457-310">インターフェイス宣言</span><span class="sxs-lookup"><span data-stu-id="72457-310">Interface declarations</span></span>

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a><span data-ttu-id="72457-311">インターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="72457-311">Interface identifiers</span></span>

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

<span data-ttu-id="72457-312">開く [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)、[IMAPISession::OpenEntry](imapisession-openentry.md) または [IMsgStore::OpenEntry](imsgstore-openentry.md) で次の 2 つのインターフェイス識別子を使用し、フォルダー オブジェクトおよびメッセージ オブジェクトそれぞれに対するプロバイダー チェックを無視します。</span><span class="sxs-lookup"><span data-stu-id="72457-312">Use the two following interface identifiers with [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), or [IMsgStore::OpenEntry](imsgstore-openentry.md) to open and ignore any provider check on a folder object and a message object, respectively.</span></span> 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a><span data-ttu-id="72457-313">MAPI ストア</span><span class="sxs-lookup"><span data-stu-id="72457-313">MAPI store</span></span>

<span data-ttu-id="72457-314">このセクションでは、MAPI ストアとインターフェイスする API で使用する、定数の定義およびインターフェイス識別子について説明します。</span><span class="sxs-lookup"><span data-stu-id="72457-314">This section contains constant definitions and interface identifiers used by APIs that interface with a MAPI store.</span></span>
  
### <a name="constants"></a><span data-ttu-id="72457-315">定数</span><span class="sxs-lookup"><span data-stu-id="72457-315">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="72457-316">fnevIndexing</span><span class="sxs-lookup"><span data-stu-id="72457-316">fnevIndexing</span></span>  <br/> |<span data-ttu-id="72457-317">((ULONG) 0x00010000)</span><span class="sxs-lookup"><span data-stu-id="72457-317">((ULONG) 0x00010000)</span></span>  <br/> |<span data-ttu-id="72457-318">ストア プロバイダーは、**[NOTIFICATION](notification.md)** 構造の **ulEventType** メンバーに **fnevIndexing** を指定して、オブジェクトがインデックスを作成する準備ができていることをインデクサーに通知できます。</span><span class="sxs-lookup"><span data-stu-id="72457-318">A store provider can specify **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure to notify the indexer that an object is ready for indexing.</span></span> <span data-ttu-id="72457-319">**NOTIFICATION** 構造の **info** メンバーには、**[EXTENDED_NOTIFICATION](extended_notification.md)** 構造が含まれます。</span><span class="sxs-lookup"><span data-stu-id="72457-319">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="72457-320">FS_NONE</span><span class="sxs-lookup"><span data-stu-id="72457-320">FS_NONE</span></span>  <br/> |<span data-ttu-id="72457-321">0x00</span><span class="sxs-lookup"><span data-stu-id="72457-321">0x00</span></span>  <br/> |<span data-ttu-id="72457-322">クライアントは **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** を呼び出すことができ、返されたビットマスクを確認できます。</span><span class="sxs-lookup"><span data-stu-id="72457-322">A client can call **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** and check for the returned bitmask.</span></span> <span data-ttu-id="72457-323">**FS_NONE** は、フォルダーが共有をサポートしていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="72457-323">**FS_NONE** indicates that the folder does not support sharing.</span></span>  <br/> |
|<span data-ttu-id="72457-324">FS_SUPPORTS_SHARING</span><span class="sxs-lookup"><span data-stu-id="72457-324">FS_SUPPORTS_SHARING</span></span>  <br/> |<span data-ttu-id="72457-325">0x01</span><span class="sxs-lookup"><span data-stu-id="72457-325">0x01</span></span>  <br/> |<span data-ttu-id="72457-326">クライアントは **IFolderSupport::GetSupportMask** を呼び出すことができ、返されたビットマスクを確認できます。</span><span class="sxs-lookup"><span data-stu-id="72457-326">A client can call **IFolderSupport::GetSupportMask** and check for the returned bitmask.</span></span> <span data-ttu-id="72457-327">**FS_SUPPORTS_SHARING** は、フォルダーが共有をサポートしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="72457-327">**FS_SUPPORTS_SHARING** indicates that the folder supports sharing.</span></span>  <br/> |
|<span data-ttu-id="72457-328">INDEXING_SEARCH_OWNER</span><span class="sxs-lookup"><span data-stu-id="72457-328">INDEXING_SEARCH_OWNER</span></span>  <br/> |<span data-ttu-id="72457-329">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="72457-329">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="72457-330">オブジェクトがインデックス作成の準備ができていることをインデクサーに通知するプロセスを識別します。</span><span class="sxs-lookup"><span data-stu-id="72457-330">Identifies the process that is pushing a notification to an indexer that an object is ready for indexing.</span></span>  <br/> |
|<span data-ttu-id="72457-331">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="72457-331">MNID_ID</span></span>  <br/> |<span data-ttu-id="72457-332">Microsoft Windows ソフトウェア開発キット (SDK) の mapidefs.h ヘッダーファイルで定義されています</span><span class="sxs-lookup"><span data-stu-id="72457-332">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h</span></span>  <br/> |<span data-ttu-id="72457-333">**[MAPINAMEID](mapinameid.md)** 構造の **ulKind** フィールドの値です。</span><span class="sxs-lookup"><span data-stu-id="72457-333">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="72457-334">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="72457-334">MNID_STRING</span></span>  <br/> |<span data-ttu-id="72457-335">Microsoft Windows ソフトウェア開発キット (SDK) の mapidefs.h ヘッダーファイルで定義されています。</span><span class="sxs-lookup"><span data-stu-id="72457-335">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h.</span></span>  <br/> |<span data-ttu-id="72457-336">**[MAPINAMEID](mapinameid.md)** 構造の **ulKind** フィールドの値です。</span><span class="sxs-lookup"><span data-stu-id="72457-336">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="72457-337">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="72457-337">MSCAP_RES_ANNOTATION</span></span>  <br/> |<span data-ttu-id="72457-338">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="72457-338">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="72457-339">クライアントが **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)** の *mscapSelector* で **MSCAP_SEL_RESTRICTION** を指定し、ストアが制限内の無効なパラメーターを無視する場合、**GetCapabilities** はこの値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="72457-339">If a client specifies **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  for **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** can return this value if the store ignores invalid parameters in a restriction.</span></span>  <br/> |
|<span data-ttu-id="72457-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="72457-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>  <br/> |<span data-ttu-id="72457-341">((ULONG) 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="72457-341">((ULONG) 0x00000020)</span></span>  <br/> |<span data-ttu-id="72457-342">クライアントが **IMSCapabilities::GetCapabilities** の *mscapSelector* で **MSCAP_SEL_FOLDER** を指定し、ストアがフォルダー ホーム ページをサポートする既定以外のストアである場合、**GetCapabilities** はこの値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="72457-342">If a client specifies **MSCAP_SEL_FOLDER** in  *mscapSelector*  for **IMSCapabilities::GetCapabilities**, **GetCapabilities** can return this value if the store is a non-default store that supports folder home pages.</span></span>  <br/> |
|<span data-ttu-id="72457-343">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="72457-343">STORE_PUSHER_OK</span></span>  <br/> |<span data-ttu-id="72457-344">((ULONG) 0x00800000)</span><span class="sxs-lookup"><span data-stu-id="72457-344">((ULONG) 0x00800000)</span></span>  <br/> |<span data-ttu-id="72457-345">クライアントは **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** プロパティを取得して、メッセージ ストアの特性を決定できます。</span><span class="sxs-lookup"><span data-stu-id="72457-345">A client can get the property **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** to determine the characteristic of a message store.</span></span> <span data-ttu-id="72457-346">ストア プロバイダーによって **STORE_PUSHER_OK** フラグがビットマスクに設定されると、MAPI プロトコル ハンドラーがストアをクロールしなくなります。この場合は、ストアが、すべての変更を通知によってインデクサーにプッシュし、メッセージのインデックスを作成することになります。</span><span class="sxs-lookup"><span data-stu-id="72457-346">If the store provider sets the **STORE_PUSHER_OK** flag in the bitmask, that means the MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>  <br/> |
   
### <a name="definitions-for-namespaces"></a><span data-ttu-id="72457-347">名前空間の定義</span><span class="sxs-lookup"><span data-stu-id="72457-347">Definitions for namespaces</span></span>

<span data-ttu-id="72457-348">次のグローバル一意識別子 (GUID) は、名前付きプロパティの名前空間を表しています。</span><span class="sxs-lookup"><span data-stu-id="72457-348">The following globally unique identifiers (GUIDs) represent the namespaces of named properties.</span></span> <span data-ttu-id="72457-349">MAPI プロトコル ハンドラー (PH) によってインデックスが作成され、読み取り専用として文書化されます。</span><span class="sxs-lookup"><span data-stu-id="72457-349">They are indexed by the MAPI Protocol Handler (PH), and are documented as read-only.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="72457-350">名前付きプロパティは、アイテムの作成や変更に使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="72457-350">The named properties should not be used to create or modify items.</span></span> 
  
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

#### <a name="mnidid-properties"></a><span data-ttu-id="72457-351">MNID_ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="72457-351">MNID_ID Properties</span></span>
  
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

#### <a name="mnidstring-properties"></a><span data-ttu-id="72457-352">MNID_STRING プロパティ</span><span class="sxs-lookup"><span data-stu-id="72457-352">MNID_STRING Properties</span></span>
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a><span data-ttu-id="72457-353">インターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="72457-353">Interface identifiers</span></span>

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

<span data-ttu-id="72457-354">Windows SDK の guiddef.h ヘッダー ファイルで定義されている `DEFINE_OLEGUID` マクロを使用して、次の GUID のシンボリック名をその値に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="72457-354">Use the  `DEFINE_OLEGUID` macro defined in the Windows SDK header file guiddef.h to associate the following GUID symbolic name with its value.</span></span> 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a><span data-ttu-id="72457-355">MAPI アドレス帳の変数</span><span class="sxs-lookup"><span data-stu-id="72457-355">MAPI Address Book</span></span>

<span data-ttu-id="72457-356">このセクションでは、MAPI アドレス帳の定数の定義について説明します。</span><span class="sxs-lookup"><span data-stu-id="72457-356">This section contains constant definitions for the MAPI Address Book.</span></span>
  
### <a name="constants"></a><span data-ttu-id="72457-357">定数</span><span class="sxs-lookup"><span data-stu-id="72457-357">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="72457-358">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="72457-358">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="72457-359">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="72457-359">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="72457-360">MAPI アドレス帳のオブジェクトのルート フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="72457-360">The root folder for a MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="72457-361">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="72457-361">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="72457-362">((ULONG) 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="72457-362">((ULONG) 0x00000002)</span></span>  <br/> |<span data-ttu-id="72457-363">MAPI アドレス帳のオブジェクトのルート フォルダー内に含まれるサブフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="72457-363">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="72457-364">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="72457-364">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="72457-365">((ULONG) 0x00000003)</span><span class="sxs-lookup"><span data-stu-id="72457-365">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="72457-366">アドレス帳のコンテナー オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="72457-366">An address book container object.</span></span>  <br/> |
|<span data-ttu-id="72457-367">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="72457-367">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="72457-368">((ULONG) 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="72457-368">((ULONG) 0x00000004)</span></span>  <br/> |<span data-ttu-id="72457-369">メッセージングを処理するユーザー オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="72457-369">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="72457-370">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="72457-370">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="72457-371">((ULONG) 0x00000005)</span><span class="sxs-lookup"><span data-stu-id="72457-371">((ULONG) 0x00000005)</span></span>  <br/> |<span data-ttu-id="72457-372">配布リスト オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="72457-372">A distribution list object.</span></span>  <br/> |
   
## <a name="additional-mapi-constants"></a><span data-ttu-id="72457-373">その他の MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="72457-373">Additional MAPI constants</span></span>

<span data-ttu-id="72457-374">このセクションでは、MAPI API で使用する定数の定義 (エラー コードを含む) とインターフェイス識別子について説明します。以下に記載されているのは、今まで未公開で文書化されていなかったものです。</span><span class="sxs-lookup"><span data-stu-id="72457-374">This section contains constant definitions including error codes, and interface identifiers used by MAPI APIs that were not previously exposed and documented.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="72457-375">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="72457-375">DIALOG_MODAL</span></span>  <br/> |<span data-ttu-id="72457-376">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="72457-376">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="72457-377">クライアントが [IAddrBook::Details](iaddrbook-details.md) メソッドを呼び出すとき、クライアントは、特定のアドレス帳エントリの詳細を示すモーダル ダイアログ ボックスを表示するために、_ulFlags_ パラメーターに **DIALOG_MODAL** フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72457-377">When a client calls the [IAddrBook::Details](iaddrbook-details.md) method, the client must set the **DIALOG_MODAL** flag in the  _ulFlags_ parameter to display the modal dialog box showing the details about a particular address book entry.</span></span> <span data-ttu-id="72457-378">この定数は mapidefs.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="72457-378">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="72457-379">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="72457-379">ITEMPROC_FORCE</span></span>  <br/> |<span data-ttu-id="72457-380">0x00000800</span><span class="sxs-lookup"><span data-stu-id="72457-380">0x00000800</span></span>  <br/> |<span data-ttu-id="72457-381">Outlook 2007 では、MAPI クライアントに新しいメッセージが通知される前に、ラップされた PST ストアによって、新しいメッセージに対するルールとスパムのフィルター処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="72457-381">In Outlook 2007, wrapped PST stores have rules and spam filtering processed on new messages before MAPI clients are notified of the new messages.</span></span> <span data-ttu-id="72457-382">[IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを使用して PST ストアに新しいメッセージを作成するプロバイダーまたはクライアントは、メッセージがルールの処理に適格であることを PST ストアに示すために、[IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドの _ulFlags_ パラメーターに **ITEMPROC_FORCE** フラグを設定する必要があります。この設定は、ストアが新しいメッセージの到着をリッスンするすべてのクライアントに通知する前に行われる必要があります。</span><span class="sxs-lookup"><span data-stu-id="72457-382">A provider or client using the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new message in PST stores should set the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to indicate to the PST store that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="72457-383">なお、このルールの処理は、Microsoft Exchange Server 以外のサーバーで作成された新しいメッセージにのみ適用されます。Exchange Server は、そのサーバー上のメッセージ用のルールを処理するからです。</span><span class="sxs-lookup"><span data-stu-id="72457-383">Note that such rules processing only applies to new messages created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="72457-384">したがって、メッセージを作成するプロバイダーまたはクライアントは、サーバーが Exchange サーバーではないことを示す **NON_EMS_XP_SAVE** と組み合わせてこのフラグを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="72457-384">Hence the provider or client creating the message must pass this flag in combination with **NON_EMS_XP_SAVE**, which indicates the server is not an Exchange server.</span></span>  <br/> |
| <span data-ttu-id="72457-385">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="72457-385">MAPI_BG_SESSION</span></span>  <br/> |<span data-ttu-id="72457-386">0x00200000</span><span class="sxs-lookup"><span data-stu-id="72457-386">0x00200000</span></span>  <br/> |<span data-ttu-id="72457-387">クライアントは [MAPILogonEx](mapilogonex.md) 関数を呼び出し、_flFlags_ パラメーターに **MAPI_BG_SESSION** フラグを設定してセッションにログオンし、バックグラウンドですべての操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="72457-387">A client can call the [MAPILogonEx](mapilogonex.md) function, setting the **MAPI_BG_SESSION** flag in the  _flFlags_ parameter to log on to a session and carry out any operations in the background.</span></span> <span data-ttu-id="72457-388">通常、クライアントがバックグラウンド スレッドまたは別のプロセスでフォアグラウンド スレッドの妨げにならないように処理を行う場合は、**MAPI_BG_SESSION** フラグを使用して [MAPILogonEx](mapilogonex.md) を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="72457-388">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call [MAPILogonEx](mapilogonex.md) with the **MAPI_BG_SESSION** flag.</span></span> <span data-ttu-id="72457-389">この例は、バックグラウンド型アクセスで個人用フォルダー ファイル (PST) を開くインデックス作成エンジンなどのクライアント アプリケーションで使用します。</span><span class="sxs-lookup"><span data-stu-id="72457-389">An example where this is used is a client application, such as an indexing engine, opening a Personal Folders File (PST) for background type access.</span></span>  <br/> |
|<span data-ttu-id="72457-390">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="72457-390">MAPI_CACHE_ONLY</span></span>  <br/> |<span data-ttu-id="72457-391">0x00004000</span><span class="sxs-lookup"><span data-stu-id="72457-391">0x00004000</span></span>  <br/> |<span data-ttu-id="72457-392">クライアントは、_ulFlags_ パラメーターに **MAPI_CACHE_ONLY** フラグを設定して、[IAddrBook::OpenEntry](iaddrbook-openentry.md) メソッドを呼び出すことができます。アドレス帳エントリを開き、その後にキャッシュからのみアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="72457-392">A client can call the [IAddrBook::OpenEntry](iaddrbook-openentry.md) method, setting the **MAPI_CACHE_ONLY** flag in the  _ulFlags_ parameter to open an address book entry and to access it subsequently only from the cache.</span></span> <span data-ttu-id="72457-393">この例は、Exchange キャッシュ モードでグローバル アドレス一覧を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスする、クライアント アプリケーションで使用します。</span><span class="sxs-lookup"><span data-stu-id="72457-393">An example where this is used is a client application that wants to open the Global Address List in Cached Exchange mode and access an entry in that Address Book from the cache without creating traffic between the client and the server.</span></span>  <br/> |
|<span data-ttu-id="72457-394">MAPI_DIALOG_MODELESS</span><span class="sxs-lookup"><span data-stu-id="72457-394">MAPI_DIALOG_MODELESS</span></span>  <br/> |<span data-ttu-id="72457-395">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="72457-395">0x0000000C</span></span>  <br/> |<span data-ttu-id="72457-396">既定のメール アプリケーションによってモードレス ダイアログ ボックスが表示されるように指定するために、この値を _ulFlags_ パラメーターの Simple MAPI MAPISendMail 関数に渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="72457-396">This value can be passed to the Simple MAPI MAPISendMail function in the  _ulFlags_ parameter to specify that a modeless dialog box is displayed by the default mail application.</span></span> <span data-ttu-id="72457-397">このフラグも MAPI_DIALOG (0x00000008) も設定されていないと、ダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="72457-397">If neither this flag nor MAPI_DIALOG (0x00000008) is set, no dialog box is displayed.</span></span>  <br/> |
|<span data-ttu-id="72457-398">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="72457-398">MAPI_NO_CACHE</span></span>  <br/> |<span data-ttu-id="72457-399">0x00000200</span><span class="sxs-lookup"><span data-stu-id="72457-399">0x00000200</span></span>  <br/> |<span data-ttu-id="72457-400">Microsoft Office Outlook が Exchange キャッシュ モードの状態で、ストアがキャッシュ モードで開かれている場合、クライアントまたはサービス プロバイダーは [IMsgStore::OpenEntry](imsgstore-openentry.md) を呼び出し、_ulFlags_ パラメーターに **MAPI_NO_CACHE** フラグを設定して、リモート ストアのアイテムまたはフォルダーを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="72457-400">If Microsoft Office Outlook is in Cached Exchange Mode and a store has been opened in cached mode, a client or service provider can call [IMsgStore::OpenEntry](imsgstore-openentry.md), setting the **MAPI_NO_CACHE** flag in the  _ulFlags_ parameter to open an item or a folder on the remote store.</span></span> <span data-ttu-id="72457-401">リモート　サーバー上の **MDB_ONLINE** フラグを使用してメッセージ ストアを開く場合は、**MAPI_NO_CACHE** フラグを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="72457-401">Note that if you open the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span>  <br/> |
|<span data-ttu-id="72457-402">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="72457-402">MAPI_UNICODE</span></span>  <br/> |<span data-ttu-id="72457-403">0x80000000</span><span class="sxs-lookup"><span data-stu-id="72457-403">0x80000000</span></span>  <br/> |<span data-ttu-id="72457-404">クライアントまたはサービス プロバイダーは [OpenIMsgOnIStg](openimsgonistg.md) 関数を呼び出し、_ulFlags_ パラメーターに **MAPI_UNICODE** フラグを設定して Unicode の .msg ファイルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="72457-404">A client or service provider can call the [OpenIMsgOnIStg](openimsgonistg.md) function, setting the **MAPI_UNICODE** flag in the  _ulFlags_ parameter to create Unicode .msg files.</span></span> <span data-ttu-id="72457-405">結果として [IMessage : IMAPIProp](imessageimapiprop.md) ファイルが作成され、このファイルは [PidTagStoreSupportMask 正規プロパティ](pidtagstoresupportmask-canonical-property.md)に **STORE_UNICODE_OK** を表示し、Unicode のプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="72457-405">The resulting [IMessage : IMAPIProp](imessageimapiprop.md) file shows **STORE_UNICODE_OK** in its [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> <span data-ttu-id="72457-406">この定数は mapidefs.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="72457-406">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="72457-407">MDB_ONLINE</span><span class="sxs-lookup"><span data-stu-id="72457-407">MDB_ONLINE</span></span>  <br/> |<span data-ttu-id="72457-408">0x00000100</span><span class="sxs-lookup"><span data-stu-id="72457-408">0x00000100</span></span>  <br/> |<span data-ttu-id="72457-409">Outlook が Exchange キャッシュ モードの場合、クライアントまたはサービス プロバイダーは [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) メソッドを呼び出し、_ulFlags_ パラメーターに **MDB_ONLINE** フラグを設定して、ローカルのメッセージ ストアへの接続を上書きし、リモート サーバー上のストアを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="72457-409">If Outlook is in Cached Exchange Mode, a client or service provider can call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method, setting the **MDB_ONLINE** flag in the  _ulFlags_ parameter to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="72457-410">なお、同じ MAPI セッションにおいて、同時にキャッシュ モードと非キャッシュ モードで Exchange ストアを開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="72457-410">Note that you cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="72457-411">キャッシュ済みのメッセージ ストアを既に開いている場合は、このフラグを使用してストアを開く前にストアを閉じるか、このフラグを使用してリモート サーバー上の Exchange ストアを開くことができる新しい MAPI セッションを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="72457-411">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>  <br/> |
|<span data-ttu-id="72457-412">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="72457-412">NON_EMS_XP_SAVE</span></span>  <br/> |<span data-ttu-id="72457-413">0x00001000</span><span class="sxs-lookup"><span data-stu-id="72457-413">0x00001000</span></span>  <br/> |<span data-ttu-id="72457-414">クライアントは [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出し、_ulFlags_ パラメーターに **NON_EMS_XP_SAVE** フラグを設定して、メッセージが Exchange サーバーから配信されなかったことを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="72457-414">A client can call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method, setting the **NON_EMS_XP_SAVE** flag in the  _ulFlags_ parameter to indicate that the message has not been delivered from an Exchange server.</span></span> <span data-ttu-id="72457-415">メッセージがルールの処理に適格であることを PST ストアに示すために、このフラグは、_ulFlags_ パラメーターの **ITEMPROC_FORCE** フラグと組み合わせて使用する必要があります。この処理は、リッスンしているすべてのクライアントに PST ストアがメッセージの到着を通知する前に行われる必要があります。</span><span class="sxs-lookup"><span data-stu-id="72457-415">This flag should be used in combination with the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter to indicate to a PST store that the message is eligible for rules processing before the PST store notifies any listening client of the arrival of the message.</span></span> <span data-ttu-id="72457-416">このルールの処理は、Exchange サーバーではないサーバー上の [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) で作成された新しいメッセージにのみ適用されます (Exchange サーバーでは、既にメッセージに対してルールが処理されています)。</span><span class="sxs-lookup"><span data-stu-id="72457-416">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange server (in which case the Exchange server would have already processed rules on the message).</span></span>  <br/> |
|<span data-ttu-id="72457-417">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="72457-417">SPAMFILTER_ONSAVE</span></span>  <br/> |<span data-ttu-id="72457-418">0x00000080</span><span class="sxs-lookup"><span data-stu-id="72457-418">0x00000080</span></span>  <br/> |<span data-ttu-id="72457-419">クライアントは [IMAPIProp::SaveChanges](imapiprop-savechanges.md) を呼び出し、_ulFlags_ パラメーターに**SPAMFILTER_ONSAVE** フラグを設定して、保存されているメッセージに関するスパムのフィルター処理を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="72457-419">A client can call [IMAPIProp::SaveChanges](imapiprop-savechanges.md), setting the **SPAMFILTER_ONSAVE** flag in the  _ulFlags_ parameter to enable spam filtering on a message that is being saved.</span></span> <span data-ttu-id="72457-420">スパムのフィルター処理に関するサポートは、送信者の電子メール アドレスの種類が簡易メール転送プロトコル (SMTP) であり、メッセージが個人用フォルダー ファイル (PST) 向けのストアに保存されている場合にのみ使用することができます。</span><span class="sxs-lookup"><span data-stu-id="72457-420">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>  <br/> |
|<span data-ttu-id="72457-421">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="72457-421">STORE_ITEMPROC</span></span>  <br/> |<span data-ttu-id="72457-422">0x00200000</span><span class="sxs-lookup"><span data-stu-id="72457-422">0x00200000</span></span>  <br/> |<span data-ttu-id="72457-423">ラップされた PST ストアの [PidTagStoreSupportMask 正規プロパティ](pidtagstoresupportmask-canonical-property.md)にこのフラグが設定されている場合、ストアに新しいメッセージが到着したときに、ストアによるルールの処理とスパムのフィルター処理がメッセージごとに別々に行われることを示します。</span><span class="sxs-lookup"><span data-stu-id="72457-423">If this flag is set in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) of a wrapped PST store, it indicates that when a new message arrives at the store, the store has rules and spam filtering processed on the message separately.</span></span> <span data-ttu-id="72457-424">それから、ストアは [IMAPISupport::Notify](imapisupport-notify.md) を呼び出し、パラメーターとして渡された [NOTIFICATION](notification.md) 構造に **fnevNewMail** を設定し、リッスンしているクライアントに新しいメッセージの詳細を渡します。</span><span class="sxs-lookup"><span data-stu-id="72457-424">The store then calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and passing the details of the new message to a listening client.</span></span> <span data-ttu-id="72457-425">その後、リッスンしているクライアントが通知を受信すれば、メッセージに対するルールの処理は行われなくなります。</span><span class="sxs-lookup"><span data-stu-id="72457-425">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span>  <br/> |
|<span data-ttu-id="72457-426">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="72457-426">STORE_UNICODE_OK</span></span>  <br/> |<span data-ttu-id="72457-427">0x00040000</span><span class="sxs-lookup"><span data-stu-id="72457-427">0x00040000</span></span>  <br/> |<span data-ttu-id="72457-428">このフラグが [PidTagStoreSupportMask 正規プロパティ](pidtagstoresupportmask-canonical-property.md)に含まれている場合、ストアが Unicode の記憶域をサポートしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="72457-428">If this flag is included in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md), it indicates that the store supports Unicode storage.</span></span> <span data-ttu-id="72457-429">クライアントは、フラグの有無を調べて、Unicode の情報を要求するかストアに保存するかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="72457-429">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span>  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a><span data-ttu-id="72457-430">フォルダー内のアイテムをアーカイブするための定義</span><span class="sxs-lookup"><span data-stu-id="72457-430">Definitions for archiving items in a folder</span></span>

<span data-ttu-id="72457-431">次の定数の定義は、[PidTagAgingGranularity 正規プロパティ](pidtagaginggranularity-canonical-property.md)の設定に使用する値です。</span><span class="sxs-lookup"><span data-stu-id="72457-431">The following constant definitions are values used to set the [PidTagAgingGranularity Canonical Property](pidtagaginggranularity-canonical-property.md).</span></span>
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a><span data-ttu-id="72457-432">リモート オブジェクトを表示するための定義</span><span class="sxs-lookup"><span data-stu-id="72457-432">Definitions for displaying remote objects</span></span>

<span data-ttu-id="72457-433">次の定数およびマクロの定義は、リモート オブジェクトを表示するためのものです。</span><span class="sxs-lookup"><span data-stu-id="72457-433">The following constant and macro definitions are for displaying remote objects.</span></span> <span data-ttu-id="72457-434">詳細については、[PidTagDisplayTypeEx 正規プロパティ](pidtagdisplaytypeex-canonical-property.md) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="72457-434">For more information, see the [PidTagDisplayTypeEx Canonical Property](pidtagdisplaytypeex-canonical-property.md).</span></span>
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a><span data-ttu-id="72457-435">Exchange のアドレス帳およびメッセージ ストアのエラー コードの定義</span><span class="sxs-lookup"><span data-stu-id="72457-435">Definitions for Exchange address book and Message store error codes</span></span>

<span data-ttu-id="72457-436">以下は、再接続機能を持つ Exchange アドレス帳とメッセージ ストアのエラーコードの定義について説明したものです。</span><span class="sxs-lookup"><span data-stu-id="72457-436">The following contains error code definitions for the Exchange Address Book and Message Store, which have reconnection capability.</span></span> <span data-ttu-id="72457-437">最後の呼び出しが切断されたグローバル カタログ (GC) への呼び出しの場合、再試行が必要となる **MAPI_E_END_OF_SESSION** エラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="72457-437">The last call to a disconnected Global Catalog (GC) may result in the **MAPI_E_END_OF_SESSION** error, which would need to be retried.</span></span> 
  
<span data-ttu-id="72457-438">Outlook の MAPI では、特別な再構成を行わずに GC サーバーに再接続することができますが、その他のエラー コードもクライアントに返されることがあります。</span><span class="sxs-lookup"><span data-stu-id="72457-438">Outlook's MAPI supports reconnection to a GC server without special reconfiguration, but some other error codes can be returned to the client.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="72457-439">MAPI_E_END_OF_SESSION</span><span class="sxs-lookup"><span data-stu-id="72457-439">MAPI_E_END_OF_SESSION</span></span>  <br/> |<span data-ttu-id="72457-440">0x80040200</span><span class="sxs-lookup"><span data-stu-id="72457-440">0x80040200</span></span>  <br/> |<span data-ttu-id="72457-441">接続が切断されたときに返されます。</span><span class="sxs-lookup"><span data-stu-id="72457-441">Returned when a connection has been disconnected.</span></span>  <br/> |
|<span data-ttu-id="72457-442">MAPI_E_RECONNECTED</span><span class="sxs-lookup"><span data-stu-id="72457-442">MAPI_E_RECONNECTED</span></span>  <br/> |<span data-ttu-id="72457-443">0x80040125</span><span class="sxs-lookup"><span data-stu-id="72457-443">0x80040125</span></span>  <br/> |<span data-ttu-id="72457-444">リモート プロシージャ コール (RPC) 接続トークンが古くなっている場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="72457-444">Returned when the Remote Procedure Call (RPC) connection token is out-of-date.</span></span> <span data-ttu-id="72457-445">現在のトランザクションのトークンが、再接続を示す接続のトークンと異なる場合は、**MAPI_E_RECONNECTED** が返され、**MAPI_E_END_OF_SESSION** と同じように扱うことができます。</span><span class="sxs-lookup"><span data-stu-id="72457-445">If the token of the current transaction is different from the token of the connection that means it has reconnected, so **MAPI_E_RECONNECTED** is returned and can be treated the same as **MAPI_E_END_OF_SESSION**.</span></span> <span data-ttu-id="72457-446">呼び出しは再試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72457-446">The call should be retried.</span></span>  <br/> |
|<span data-ttu-id="72457-447">MAPI_E_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="72457-447">MAPI_E_OFFLINE</span></span>  <br/> |<span data-ttu-id="72457-448">0x80040126</span><span class="sxs-lookup"><span data-stu-id="72457-448">0x80040126</span></span>  <br/> |<span data-ttu-id="72457-449">接続がオフラインのときに返されます。</span><span class="sxs-lookup"><span data-stu-id="72457-449">Returned when the connection is offline.</span></span> <span data-ttu-id="72457-450">通常、サーバーの障害やネットワーク接続の切断など、環境内に何かが発生したことを意味します。</span><span class="sxs-lookup"><span data-stu-id="72457-450">Typically this means that something has occurred in the environment, such as server failure or loss of network connectivity.</span></span> <span data-ttu-id="72457-451">このエラーは、キャッシュ モードのプロファイルを使用して、サーバーと通信するためにキャッシュをバイパスしようとしたときに最も発生しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="72457-451">This error is most likely to occur when using a cached mode profile and attempting to bypass the cache to communicate with the server.</span></span> <span data-ttu-id="72457-452">キャッシュによって最初にサーバーとの接続を確立できなかった場合は、オフライン状態になっている可能性があります。その場合、**MAPI_E_OFFLINE** が現れます。</span><span class="sxs-lookup"><span data-stu-id="72457-452">If the cache was never able to initially establish a connection to the server, it may be in the offline state in which **MAPI_E_OFFLINE** could surface.</span></span>  <br/> |
   
<span data-ttu-id="72457-453">上記に該当する可能性のあるすべてのシナリオの場合、上記 2 つのエラーはいずれも返されません。</span><span class="sxs-lookup"><span data-stu-id="72457-453">Neither of the preceding two errors will be returned in all scenarios where they would likely appear to apply.</span></span> <span data-ttu-id="72457-454">ほとんどの場合、**MAPI\_E_NETWORK_ERROR** または **MAPI_E_CALL_FAILED** が返されます。</span><span class="sxs-lookup"><span data-stu-id="72457-454">In most cases, **MAPI\_E_NETWORK_ERROR** or **MAPI_E_CALL_FAILED** will be returned.</span></span> <span data-ttu-id="72457-455">[Microsoft Exchange Server MAPI クライアントと Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440) のダウンロードを使用すれば、いずれも表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="72457-455">Neither will appear using the [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440) download.</span></span> 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a><span data-ttu-id="72457-456">Exchange Server メールボックスのキャッシュ モードのクォータに関する定義</span><span class="sxs-lookup"><span data-stu-id="72457-456">Definitions for Exchange Server Mailbox cached mode quotas</span></span>

<span data-ttu-id="72457-457">次の定数の定義は、Microsoft Outlook 2010 および Microsoft Outlook 2013 で使用します。Microsoft Outlook 2010 および Microsoft Outlook 2013 以外の場合にオンライン プロファイルでのみ使用できる Exchange メールボックス クォータと同等の、Exchange のキャッシュ モードにおけるプロファイルのクォータを設定します。</span><span class="sxs-lookup"><span data-stu-id="72457-457">The following constant definitions are used by Microsoft Outlook 2010 and Microsoft Outlook 2013 to set the Exchange cached mode profile quotas that are equivalent to the Exchange mailbox quotas otherwise available only with an online profile.</span></span>
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

<span data-ttu-id="72457-458">これらのプロパティは、対応するオンライン プロパティにマップされ、キロバイト単位の同じ値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="72457-458">These properties map to their correspondent online properties and contain the same values in kilobytes.</span></span> <span data-ttu-id="72457-459">PR_QUOTA_WARNING は PR_STORAGE_QUOTA_LIMIT に、PR_QUOTA_SEND は PR_QUOTA_PROHIBIT_SEND_QUOTA に、PR_QUOTA_RECEIVE は PR_PROHIBIT_RECEIVE_QUOTA にそれぞれマップされます。</span><span class="sxs-lookup"><span data-stu-id="72457-459">PR_QUOTA_WARNING maps to PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND to PR_QUOTA_PROHIBIT_SEND_QUOTA, and PR_QUOTA_RECEIVE to PR_PROHIBIT_RECEIVE_QUOTA.</span></span>
  
### <a name="definitions-for-message-format"></a><span data-ttu-id="72457-460">メッセージ形式の定義</span><span class="sxs-lookup"><span data-stu-id="72457-460">Definitions for message format</span></span>

<span data-ttu-id="72457-461">次の定数の定義は、[PidTagMessageEditorFormat 正規プロパティ](pidtagmessageeditorformat-canonical-property.md)の設定に使用する値です。</span><span class="sxs-lookup"><span data-stu-id="72457-461">The following constant definitions are values that are used to set the [PidTagMessageEditorFormat Canonical Property](pidtagmessageeditorformat-canonical-property.md).</span></span>
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a><span data-ttu-id="72457-462">RPC over HTTP の使用の定義</span><span class="sxs-lookup"><span data-stu-id="72457-462">Definitions for using RPC over HTTP</span></span>

<span data-ttu-id="72457-463">プロパティを設定するフラグとして使用する定数の定義については、「[PidTagRpcOverHttpFlags 正規プロパティ](pidtagrpcoverhttpflags-canonical-property.md)」のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72457-463">See the [PidTagRpcOverHttpFlags Canonical Property](pidtagrpcoverhttpflags-canonical-property.md) topic for constant definitions used as flags to set the property.</span></span> 
  
<span data-ttu-id="72457-464">プロパティの設定に使用する定数の定義については、「[PidTagRpcOverHttpProxyAuthScheme 正規プロパティ](pidtagrpcoverhttpproxyauthscheme-canonical-property.md)」のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72457-464">See the [PidTagRpcOverHttpProxyAuthScheme Canonical Property](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) topic for constant definitions used to set the property.</span></span> 
  
### <a name="identifiers"></a><span data-ttu-id="72457-465">識別子</span><span class="sxs-lookup"><span data-stu-id="72457-465">Identifiers</span></span>

<span data-ttu-id="72457-466">Microsoft Windows ソフトウェア開発キット (SDK) の guiddef.h ヘッダー ファイルで定義されている `DEFINE_OLEGUID` マクロを使用して、次のグローバル一意識別子 (GUID) のシンボリック名とその値を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="72457-466">Use the  `DEFINE_OLEGUID` macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the following GUID symbolic names with their values.</span></span> 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

<span data-ttu-id="72457-467">次の識別子は、アドレス帳の Capone Profile セクション用で、複数の Exchange ([MultiEx](using-multiple-exchange-accounts.md)) メールボックスのサポートに使用され、[PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) プロパティが含まれます。このプロパティは [SetDefaultDir](iaddrbook-setdefaultdir.md) によって指定された既定のコンテナーを事実上無効にします。</span><span class="sxs-lookup"><span data-stu-id="72457-467">The following Identifier is for the Capone Profile section of an Address Book, which in support of multiple Exchange ([MultiEx](using-multiple-exchange-accounts.md)) mailboxes contains a [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property that effectively turns off the default container specified by [SetDefaultDir](iaddrbook-setdefaultdir.md).</span></span>
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a><span data-ttu-id="72457-468">インターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="72457-468">Interface identifiers</span></span>

#### <a name="imapisync"></a><span data-ttu-id="72457-469">IMAPISync</span><span class="sxs-lookup"><span data-stu-id="72457-469">IMAPISync : SynchronizeInBackground</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a><span data-ttu-id="72457-470">IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="72457-470">IMAPISyncProgressCallback::Done</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a><span data-ttu-id="72457-471">IID_IContabAdmin</span><span class="sxs-lookup"><span data-stu-id="72457-471">IID_IContabAdmin</span></span>
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a><span data-ttu-id="72457-472">IID_IMAPISECUREMESSAGE</span><span class="sxs-lookup"><span data-stu-id="72457-472">IID_IMAPISECUREMESSAGE</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a><span data-ttu-id="72457-473">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="72457-473">IID_IMAPIGetSession</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a><span data-ttu-id="72457-474">PST 上書きハンドラーのインターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="72457-474">PST Override Handler interface identifiers</span></span>

#### <a name="iidipstoverridereq"></a><span data-ttu-id="72457-475">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="72457-475">IID_IPSTOVERRIDEREQ</span></span>
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a><span data-ttu-id="72457-476">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="72457-476">IID_IPSTOVERRIDE1</span></span>
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a><span data-ttu-id="72457-477">関連項目</span><span class="sxs-lookup"><span data-stu-id="72457-477">See also</span></span>

- [<span data-ttu-id="72457-478">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="72457-478">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="72457-479">Outlook で使用される名前付きプロパティについて</span><span class="sxs-lookup"><span data-stu-id="72457-479">About Named Properties Used by Outlook</span></span>](about-named-properties-used-by-outlook.md)
- [<span data-ttu-id="72457-480">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする</span><span class="sxs-lookup"><span data-stu-id="72457-480">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="72457-481">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く</span><span class="sxs-lookup"><span data-stu-id="72457-481">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="72457-482">Exchange キャッシュ モードで同期を呼び出すことなく OST でメッセージを管理する</span><span class="sxs-lookup"><span data-stu-id="72457-482">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

