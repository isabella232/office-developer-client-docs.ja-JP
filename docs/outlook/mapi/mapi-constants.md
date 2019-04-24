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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318922"
---
# <a name="mapi-constants"></a>MAPI 定数

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、MAPI API で使用する定数の定義、MAPI インターフェイス宣言、クラスとインターフェイス識別子について説明します。
  
## <a name="class-and-interface-identifiers"></a>クラスとインターフェイス識別子

他の指定がなければ、Microsoft Windows ソフトウェア開発キット (SDK) の guiddef.h ヘッダー ファイルで定義されている DEFINE_GUID マクロを使用して、グローバル一意識別子 (GUID) のシンボリック名とその値を関連付けます。
  
## <a name="attachment-security-conversion-api"></a>添付ファイル セキュリティ変換 API

このセクションでは、添付ファイル セキュリティ API に関する定数の定義とインターフェイス識別子について説明します。
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

純粋仮想関数 **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)** を定義するには、Windows SDK の mapidefs.h ヘッダー ファイルで定義されている MAPIMETHOD マクロを使用します。 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

**[IAttachmentSecurity](iattachmentsecurityiunknown.md)** の仮想メソッド テーブルを定義するには、Windows SDK の mapidefs.h ヘッダー ファイルで定義されている DECLARE_MAPI_INTERFACE_ マクロを使用します。 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a>MAPI-MIME 会話 API

このセクションでは、MAPI-MIME 会話 API に関する定数の定義、クラスとインターフェイス識別子について説明します。
  
### <a name="constants"></a>定数

|||
|:-----|:-----|
|CCSF_SMTP  <br/> |0x0002  <br/> |
|CCSF_NOHEADERS  <br/> |0x0004  <br/> |
|CCSF_USE_TNEF  <br/> | 0x0010  <br/> |
|CCSF_INCLUDE_BCC  <br/> |0x0020  <br/> |
|CCSF_8BITHEADERS  <br/> | 0x0040  <br/> |
|CCSF_USE_RTF  <br/> |0x0080  <br/> |
|CCSF_PLAIN_TEXT_ONLY  <br/> |0x1000  <br/> |
|CCSF_NO_MSGID  <br/> |0x4000  <br/> |
|CCSF_GLOBAL_MESSAGE  <br/> |0x00200000  <br/> |
|E_INVALIDARG  <br/> | *Microsoft Windows ソフトウェア開発キット (SDK) の winerror.h ヘッダーファイルで定義されています*  <br/> |
   
### <a name="class-identifiers"></a>クラス識別子

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a>インターフェイス識別子

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a>オフライン状態 API

このセクションでは、オフライン状態 API に関する定数の定義、クラスとインターフェイス識別子について説明します。
  
### <a name="constants"></a>定数

|||
|:-----|:-----|
|E_INVALIDARG  <br/> | *Microsoft Windows ソフトウェア開発キット (SDK) の winerror.h ヘッダーファイルで定義されています*  <br/> |
|E_NOINTERFACE  <br/> | *Windows (SDK) の winerror.h ヘッダー ファイルで定義されています*  <br/> |
|MAPIOFFLINE_ADVISE_DEFAULT  <br/> |(ULONG) 0  <br/> |
|MAPIOFFLINE_UNADVISE_DEFAULT  <br/> |(ULONG) 0  <br/> |
|MAPIOFFLINE_ADVISE_TYPE_STATECHANGE  <br/> |1-d  <br/> |
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |0x1  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |0x2  <br/> |
|MAPIOFFLINE_FLAG_BLOCK  <br/> |0x00002000  <br/> |
|MAPIOFFLINE_FLAG_DEFAULT  <br/> |0x00000000  <br/> |
|MAPIOFFLINE_STATE_ALL  <br/> |0x003f037f  <br/> |
|**オンラインまたはオフライン** <br/> ||
|MAPIOFFLINE_STATE_OFFLINE_MASK  <br/> |0x00000003  <br/> |
|MAPIOFFLINE_STATE_OFFLINE  <br/> |0x00000001  <br/> |
|MAPIOFFLINE_STATE_ONLINE  <br/> |0x00000002  <br/> |
   
### <a name="class-identifiers"></a>クラス識別子

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a>インターフェイス識別子

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

## <a name="outlook-named-properties"></a>Outlook の名前付きプロパティ

このセクションでは、名前付きプロパティとその名前空間に関する定数の定義、および関連する他の定数について説明します。
  
### <a name="definitions-for-named-properties"></a>名前付きプロパティの定義

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

### <a name="definitions-for-namespaces"></a>名前空間の定義

次のグローバル一意識別子 (GUID) は、名前付きプロパティの名前空間を表しています。
  
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

PSETID の定義については、MAPI ストアのセクションを参照してください。
  
### <a name="other-constants"></a>その他の定数

|||
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0xD000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x2000000  <br/> |
|MNID_ID  <br/> | *mapidefs.h ヘッダー ファイルで定義されています。*  <br/> |
|MNID_STRING  <br/> | *mapidefs.h ヘッダー ファイルで定義されています。*  <br/> |
|mtgNone  <br/> |0x0  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |
|mtgFullUpdate  <br/> |0x00010000  <br/> |
|mtgInfoUpdate  <br/> |0x00020000  <br/> |
|mtgOutofDate  <br/> |0x00080000  <br/> |
|mtgDelegated  <br/> |0x00100000  <br/> |
   
## <a name="replication-api"></a>レプリケーション API

このセクションでは、レプリケーション API に関する定数の定義、MAPI インターフェイス宣言、クラスとインターフェイス識別子について説明します。
  
### <a name="constants"></a>定数

以下は、MAPI サービス プロバイダーを特定する [MAPIUID](mapiuid.md) 構造です。 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|DNH_OK  <br/> |0x00010000  <br/> |
|DNT_OK  <br/> |0x00010000  <br/> |
|HSF_LOCAL  <br/> |0x00000008  <br/> |
|HSF_COPYDESTRUCTIVE  <br/> |0x00000010  <br/> |
|HSF_OK  <br/> |0x00010000  <br/> |
|MDB_OST_LOGON_UNICODE  <br/> |((ULONG) 0x00000800)  <br/> |
|MDB_OST_LOGON_ANSI  <br/> |((ULONG) 0x00001000)  <br/> |
|SHOW_SOFT_DELETES  <br/> |((ULONG) 0x00000002)  <br/> |
|SS_ACTIVE  <br/> |.0  <br/> |
|SS_SUSPENDED  <br/> |1-d  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |
|SYNC_BACKGROUND  <br/> |0x00001000  <br/> |
|SYNC_THESE_FOLDERS  <br/> |0x00020000  <br/> |
|SYNC_HEADERS  <br/> |0x02000000  <br/> |
|UPC_OK  <br/> |0x00010000  <br/> |
|UPD_ASSOC  <br/> |0x00000001  <br/> |
|UPD_MOV  <br/> |0x00000002  <br/> |
|UPD_OK  <br/> |0x00010000  <br/> |
|UPD_MOVED  <br/> |0x00020000  <br/> |
|UPD_UPDATE  <br/> |0x00040000  <br/> |
|UPD_COMMIT  <br/> |0x00080000  <br/> |
|UPF_NEW  <br/> |0x00000001  <br/> |
|UPF_MOD_PARENT  <br/> |0x00000002  <br/> |
|UPF_MOD_PROPS  <br/> |0x00000004  <br/> |
|UPF_DEL  <br/> |0x00000008  <br/> |
|UPF_OK  <br/> |0x00010000  <br/> |
|UPH_OK  <br/> |0x00010000  <br/> |
|UPM_ASSOC  <br/> |0x00000001  <br/> |
|UPM_NEW  <br/> |0x00000002  <br/> |
|UPM_MOV  <br/> |0x00000004  <br/> |
|UPM_MOD_PROPS  <br/> |0x00000008  <br/> |
|UPM_HEADER  <br/> |0x00000010  <br/> |
|UPM_OK  <br/> |0x00010000  <br/> |
|UPM_MOVED  <br/> |0x00020000  <br/> |
|UPM_COMMIT  <br/> |0x00040000  <br/> |
|UPM_DELETE  <br/> |0x00080000  <br/> |
|UPM_SAVE  <br/> |0x00100000  <br/> |
|UPR_ASSOC  <br/> |0x00000001  <br/> |
|UPR_READ  <br/> |0x00000002  <br/> |
|UPR_OK  <br/> |0x00010000  <br/> |
|UPR_COMMIT  <br/> |0x00020000  <br/> |
|UPS_UPLOAD_ONLY  <br/> |0x00000001  <br/> |
|UPS_DNLOAD_ONLY  <br/> |0x00000002  <br/> |
|UPS_ONE_FOLDER  <br/> |0x00000004  <br/> |
|UPS_THESE_FOLDERS  <br/> |0x00000080  <br/> |
|UPS_OK  <br/> |0x00010000  <br/> |
|UPT_OK  <br/> |0x00010000  <br/> |
|UPT_PUBLIC  <br/> |0x00000001  <br/> |
|UPV_ERROR  <br/> |0x00010000  <br/> |
|UPV_DIRTY  <br/> |0x00020000  <br/> |
|UPV_COMMIT  <br/> |0x00040000  <br/> |
   
### <a name="interface-declarations"></a>インターフェイス宣言

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a>インターフェイス識別子

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

開く [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)、[IMAPISession::OpenEntry](imapisession-openentry.md) または [IMsgStore::OpenEntry](imsgstore-openentry.md) で次の 2 つのインターフェイス識別子を使用し、フォルダー オブジェクトおよびメッセージ オブジェクトそれぞれに対するプロバイダー チェックを無視します。 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a>MAPI ストア

このセクションでは、MAPI ストアとインターフェイスする API で使用する、定数の定義およびインターフェイス識別子について説明します。
  
### <a name="constants"></a>定数

||||
|:-----|:-----|:-----|
|fnevIndexing  <br/> |((ULONG) 0x00010000)  <br/> |ストア プロバイダーは、**[NOTIFICATION](notification.md)** 構造の **ulEventType** メンバーに **fnevIndexing** を指定して、オブジェクトがインデックスを作成する準備ができていることをインデクサーに通知できます。 **NOTIFICATION** 構造の **info** メンバーには、**[EXTENDED_NOTIFICATION](extended_notification.md)** 構造が含まれます。  <br/> |
|FS_NONE  <br/> |0x00  <br/> |クライアントは **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** を呼び出すことができ、返されたビットマスクを確認できます。 **FS_NONE** は、フォルダーが共有をサポートしていないことを示します。  <br/> |
|FS_SUPPORTS_SHARING  <br/> |0x01  <br/> |クライアントは **IFolderSupport::GetSupportMask** を呼び出すことができ、返されたビットマスクを確認できます。 **FS_SUPPORTS_SHARING** は、フォルダーが共有をサポートしていることを示します。  <br/> |
|INDEXING_SEARCH_OWNER  <br/> |((ULONG) 0x00000001)  <br/> |オブジェクトがインデックス作成の準備ができていることをインデクサーに通知するプロセスを識別します。  <br/> |
|MNID_ID  <br/> |Microsoft Windows ソフトウェア開発キット (SDK) の mapidefs.h ヘッダーファイルで定義されています  <br/> |**[MAPINAMEID](mapinameid.md)** 構造の **ulKind** フィールドの値です。  <br/> |
|MNID_STRING  <br/> |Microsoft Windows ソフトウェア開発キット (SDK) の mapidefs.h ヘッダーファイルで定義されています。  <br/> |**[MAPINAMEID](mapinameid.md)** 構造の **ulKind** フィールドの値です。  <br/> |
|MSCAP_RES_ANNOTATION  <br/> |((ULONG) 0x00000001)  <br/> |クライアントが **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)** の *mscapSelector* で **MSCAP_SEL_RESTRICTION** を指定し、ストアが制限内の無効なパラメーターを無視する場合、**GetCapabilities** はこの値を返すことができます。  <br/> |
|MSCAP_SECURE_FOLDER_HOMEPAGES  <br/> |((ULONG) 0x00000020)  <br/> |クライアントが **IMSCapabilities::GetCapabilities** の *mscapSelector* で **MSCAP_SEL_FOLDER** を指定し、ストアがフォルダー ホーム ページをサポートする既定以外のストアである場合、**GetCapabilities** はこの値を返すことができます。  <br/> |
|STORE_PUSHER_OK  <br/> |((ULONG) 0x00800000)  <br/> |クライアントは **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** プロパティを取得して、メッセージ ストアの特性を決定できます。 ストア プロバイダーによって **STORE_PUSHER_OK** フラグがビットマスクに設定されると、MAPI プロトコル ハンドラーがストアをクロールしなくなります。この場合は、ストアが、すべての変更を通知によってインデクサーにプッシュし、メッセージのインデックスを作成することになります。  <br/> |
   
### <a name="definitions-for-namespaces"></a>名前空間の定義

次のグローバル一意識別子 (GUID) は、名前付きプロパティの名前空間を表しています。 MAPI プロトコル ハンドラー (PH) によってインデックスが作成され、読み取り専用として文書化されます。
  
> [!CAUTION]
> 名前付きプロパティは、アイテムの作成や変更に使用しないでください。 
  
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

#### <a name="mnidid-properties"></a>MNID_ID プロパティ
  
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

#### <a name="mnidstring-properties"></a>MNID_STRING プロパティ
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a>インターフェイス識別子

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

Windows SDK の guiddef.h ヘッダー ファイルで定義されている `DEFINE_OLEGUID` マクロを使用して、次の GUID のシンボリック名をその値に関連付けます。 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a>MAPI アドレス帳の変数

このセクションでは、MAPI アドレス帳の定数の定義について説明します。
  
### <a name="constants"></a>定数

||||
|:-----|:-----|:-----|
|CONTAB_ROOT  <br/> |((ULONG) 0x00000001)  <br/> |MAPI アドレス帳のオブジェクトのルート フォルダーです。  <br/> |
|CONTAB_SUBROOT  <br/> |((ULONG) 0x00000002)  <br/> |MAPI アドレス帳のオブジェクトのルート フォルダー内に含まれるサブフォルダーです。  <br/> |
|CONTAB_CONTAINER  <br/> |((ULONG) 0x00000003)  <br/> |アドレス帳のコンテナー オブジェクトです。  <br/> |
|CONTAB_USER  <br/> |((ULONG) 0x00000004)  <br/> |メッセージングを処理するユーザー オブジェクトです。  <br/> |
|CONTAB_DISTLIST  <br/> |((ULONG) 0x00000005)  <br/> |配布リスト オブジェクトです。  <br/> |
   
## <a name="additional-mapi-constants"></a>その他の MAPI 定数

このセクションでは、MAPI API で使用する定数の定義 (エラー コードを含む) とインターフェイス識別子について説明します。以下に記載されているのは、今まで未公開で文書化されていなかったものです。
  
||||
|:-----|:-----|:-----|
|DIALOG_MODAL  <br/> |((ULONG) 0x00000001)  <br/> |クライアントが [IAddrBook::Details](iaddrbook-details.md) メソッドを呼び出すとき、クライアントは、特定のアドレス帳エントリの詳細を示すモーダル ダイアログ ボックスを表示するために、_ulFlags_ パラメーターに **DIALOG_MODAL** フラグを設定する必要があります。 この定数は mapidefs.h で定義されます。  <br/> |
|ITEMPROC_FORCE  <br/> |0x00000800  <br/> |Outlook 2007 では、MAPI クライアントに新しいメッセージが通知される前に、ラップされた PST ストアによって、新しいメッセージに対するルールとスパムのフィルター処理が行われます。 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを使用して PST ストアに新しいメッセージを作成するプロバイダーまたはクライアントは、メッセージがルールの処理に適格であることを PST ストアに示すために、[IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドの _ulFlags_ パラメーターに **ITEMPROC_FORCE** フラグを設定する必要があります。この設定は、ストアが新しいメッセージの到着をリッスンするすべてのクライアントに通知する前に行われる必要があります。 なお、このルールの処理は、Microsoft Exchange Server 以外のサーバーで作成された新しいメッセージにのみ適用されます。Exchange Server は、そのサーバー上のメッセージ用のルールを処理するからです。 したがって、メッセージを作成するプロバイダーまたはクライアントは、サーバーが Exchange サーバーではないことを示す **NON_EMS_XP_SAVE** と組み合わせてこのフラグを渡す必要があります。  <br/> |
| MAPI_BG_SESSION  <br/> |0x00200000  <br/> |クライアントは [MAPILogonEx](mapilogonex.md) 関数を呼び出し、_flFlags_ パラメーターに **MAPI_BG_SESSION** フラグを設定してセッションにログオンし、バックグラウンドですべての操作を実行できます。 通常、クライアントがバックグラウンド スレッドまたは別のプロセスでフォアグラウンド スレッドの妨げにならないように処理を行う場合は、**MAPI_BG_SESSION** フラグを使用して [MAPILogonEx](mapilogonex.md) を呼び出す必要があります。 この例は、バックグラウンド型アクセスで個人用フォルダー ファイル (PST) を開くインデックス作成エンジンなどのクライアント アプリケーションで使用します。  <br/> |
|MAPI_CACHE_ONLY  <br/> |0x00004000  <br/> |クライアントは、_ulFlags_ パラメーターに **MAPI_CACHE_ONLY** フラグを設定して、[IAddrBook::OpenEntry](iaddrbook-openentry.md) メソッドを呼び出すことができます。アドレス帳エントリを開き、その後にキャッシュからのみアクセスすることができます。 この例は、Exchange キャッシュ モードでグローバル アドレス一覧を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスする、クライアント アプリケーションで使用します。  <br/> |
|MAPI_DIALOG_MODELESS  <br/> |0x0000000C  <br/> |既定のメール アプリケーションによってモードレス ダイアログ ボックスが表示されるように指定するために、この値を _ulFlags_ パラメーターの Simple MAPI MAPISendMail 関数に渡すことができます。 このフラグも MAPI_DIALOG (0x00000008) も設定されていないと、ダイアログ ボックスは表示されません。  <br/> |
|MAPI_NO_CACHE  <br/> |0x00000200  <br/> |Microsoft Office Outlook が Exchange キャッシュ モードの状態で、ストアがキャッシュ モードで開かれている場合、クライアントまたはサービス プロバイダーは [IMsgStore::OpenEntry](imsgstore-openentry.md) を呼び出し、_ulFlags_ パラメーターに **MAPI_NO_CACHE** フラグを設定して、リモート ストアのアイテムまたはフォルダーを開くことができます。 リモート　サーバー上の **MDB_ONLINE** フラグを使用してメッセージ ストアを開く場合は、**MAPI_NO_CACHE** フラグを使用する必要はありません。  <br/> |
|MAPI_UNICODE  <br/> |0x80000000  <br/> |クライアントまたはサービス プロバイダーは [OpenIMsgOnIStg](openimsgonistg.md) 関数を呼び出し、_ulFlags_ パラメーターに **MAPI_UNICODE** フラグを設定して Unicode の .msg ファイルを作成できます。 結果として [IMessage : IMAPIProp](imessageimapiprop.md) ファイルが作成され、このファイルは [PidTagStoreSupportMask 正規プロパティ](pidtagstoresupportmask-canonical-property.md)に **STORE_UNICODE_OK** を表示し、Unicode のプロパティをサポートします。 この定数は mapidefs.h で定義されます。  <br/> |
|MDB_ONLINE  <br/> |0x00000100  <br/> |Outlook が Exchange キャッシュ モードの場合、クライアントまたはサービス プロバイダーは [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) メソッドを呼び出し、_ulFlags_ パラメーターに **MDB_ONLINE** フラグを設定して、ローカルのメッセージ ストアへの接続を上書きし、リモート サーバー上のストアを開くことができます。 なお、同じ MAPI セッションにおいて、同時にキャッシュ モードと非キャッシュ モードで Exchange ストアを開くことはできません。 キャッシュ済みのメッセージ ストアを既に開いている場合は、このフラグを使用してストアを開く前にストアを閉じるか、このフラグを使用してリモート サーバー上の Exchange ストアを開くことができる新しい MAPI セッションを開く必要があります。  <br/> |
|NON_EMS_XP_SAVE  <br/> |0x00001000  <br/> |クライアントは [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出し、_ulFlags_ パラメーターに **NON_EMS_XP_SAVE** フラグを設定して、メッセージが Exchange サーバーから配信されなかったことを示すことができます。 メッセージがルールの処理に適格であることを PST ストアに示すために、このフラグは、_ulFlags_ パラメーターの **ITEMPROC_FORCE** フラグと組み合わせて使用する必要があります。この処理は、リッスンしているすべてのクライアントに PST ストアがメッセージの到着を通知する前に行われる必要があります。 このルールの処理は、Exchange サーバーではないサーバー上の [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) で作成された新しいメッセージにのみ適用されます (Exchange サーバーでは、既にメッセージに対してルールが処理されています)。  <br/> |
|SPAMFILTER_ONSAVE  <br/> |0x00000080  <br/> |クライアントは [IMAPIProp::SaveChanges](imapiprop-savechanges.md) を呼び出し、_ulFlags_ パラメーターに**SPAMFILTER_ONSAVE** フラグを設定して、保存されているメッセージに関するスパムのフィルター処理を有効にすることができます。 スパムのフィルター処理に関するサポートは、送信者の電子メール アドレスの種類が簡易メール転送プロトコル (SMTP) であり、メッセージが個人用フォルダー ファイル (PST) 向けのストアに保存されている場合にのみ使用することができます。  <br/> |
|STORE_ITEMPROC  <br/> |0x00200000  <br/> |ラップされた PST ストアの [PidTagStoreSupportMask 正規プロパティ](pidtagstoresupportmask-canonical-property.md)にこのフラグが設定されている場合、ストアに新しいメッセージが到着したときに、ストアによるルールの処理とスパムのフィルター処理がメッセージごとに別々に行われることを示します。 それから、ストアは [IMAPISupport::Notify](imapisupport-notify.md) を呼び出し、パラメーターとして渡された [NOTIFICATION](notification.md) 構造に **fnevNewMail** を設定し、リッスンしているクライアントに新しいメッセージの詳細を渡します。 その後、リッスンしているクライアントが通知を受信すれば、メッセージに対するルールの処理は行われなくなります。  <br/> |
|STORE_UNICODE_OK  <br/> |0x00040000  <br/> |このフラグが [PidTagStoreSupportMask 正規プロパティ](pidtagstoresupportmask-canonical-property.md)に含まれている場合、ストアが Unicode の記憶域をサポートしていることを示します。 クライアントは、フラグの有無を調べて、Unicode の情報を要求するかストアに保存するかを決定できます。  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a>フォルダー内のアイテムをアーカイブするための定義

次の定数の定義は、[PidTagAgingGranularity 正規プロパティ](pidtagaginggranularity-canonical-property.md)の設定に使用する値です。
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a>リモート オブジェクトを表示するための定義

次の定数およびマクロの定義は、リモート オブジェクトを表示するためのものです。 詳細については、[PidTagDisplayTypeEx 正規プロパティ](pidtagdisplaytypeex-canonical-property.md) をご覧ください。
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a>Exchange のアドレス帳およびメッセージ ストアのエラー コードの定義

以下は、再接続機能を持つ Exchange アドレス帳とメッセージ ストアのエラーコードの定義について説明したものです。 最後の呼び出しが切断されたグローバル カタログ (GC) への呼び出しの場合、再試行が必要となる **MAPI_E_END_OF_SESSION** エラーが発生する可能性があります。 
  
Outlook の MAPI では、特別な再構成を行わずに GC サーバーに再接続することができますが、その他のエラー コードもクライアントに返されることがあります。
  
||||
|:-----|:-----|:-----|
|MAPI_E_END_OF_SESSION  <br/> |0x80040200  <br/> |接続が切断されたときに返されます。  <br/> |
|MAPI_E_RECONNECTED  <br/> |0x80040125  <br/> |リモート プロシージャ コール (RPC) 接続トークンが古くなっている場合に返されます。 現在のトランザクションのトークンが、再接続を示す接続のトークンと異なる場合は、**MAPI_E_RECONNECTED** が返され、**MAPI_E_END_OF_SESSION** と同じように扱うことができます。 呼び出しは再試行する必要があります。  <br/> |
|MAPI_E_OFFLINE  <br/> |0x80040126  <br/> |接続がオフラインのときに返されます。 通常、サーバーの障害やネットワーク接続の切断など、環境内に何かが発生したことを意味します。 このエラーは、キャッシュ モードのプロファイルを使用して、サーバーと通信するためにキャッシュをバイパスしようとしたときに最も発生しやすくなります。 キャッシュによって最初にサーバーとの接続を確立できなかった場合は、オフライン状態になっている可能性があります。その場合、**MAPI_E_OFFLINE** が現れます。  <br/> |
   
上記に該当する可能性のあるすべてのシナリオの場合、上記 2 つのエラーはいずれも返されません。 ほとんどの場合、**MAPI\_E_NETWORK_ERROR** または **MAPI_E_CALL_FAILED** が返されます。 [Microsoft Exchange Server MAPI クライアントと Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440) のダウンロードを使用すれば、いずれも表示されなくなります。 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a>Exchange Server メールボックスのキャッシュ モードのクォータに関する定義

次の定数の定義は、Microsoft Outlook 2010 および Microsoft Outlook 2013 で使用します。Microsoft Outlook 2010 および Microsoft Outlook 2013 以外の場合にオンライン プロファイルでのみ使用できる Exchange メールボックス クォータと同等の、Exchange のキャッシュ モードにおけるプロファイルのクォータを設定します。
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

これらのプロパティは、対応するオンライン プロパティにマップされ、キロバイト単位の同じ値が含まれます。 PR_QUOTA_WARNING は PR_STORAGE_QUOTA_LIMIT に、PR_QUOTA_SEND は PR_QUOTA_PROHIBIT_SEND_QUOTA に、PR_QUOTA_RECEIVE は PR_PROHIBIT_RECEIVE_QUOTA にそれぞれマップされます。
  
### <a name="definitions-for-message-format"></a>メッセージ形式の定義

次の定数の定義は、[PidTagMessageEditorFormat 正規プロパティ](pidtagmessageeditorformat-canonical-property.md)の設定に使用する値です。
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a>RPC over HTTP の使用の定義

プロパティを設定するフラグとして使用する定数の定義については、「[PidTagRpcOverHttpFlags 正規プロパティ](pidtagrpcoverhttpflags-canonical-property.md)」のトピックを参照してください。 
  
プロパティの設定に使用する定数の定義については、「[PidTagRpcOverHttpProxyAuthScheme 正規プロパティ](pidtagrpcoverhttpproxyauthscheme-canonical-property.md)」のトピックを参照してください。 
  
### <a name="identifiers"></a>識別子

Microsoft Windows ソフトウェア開発キット (SDK) の guiddef.h ヘッダー ファイルで定義されている `DEFINE_OLEGUID` マクロを使用して、次のグローバル一意識別子 (GUID) のシンボリック名とその値を関連付けます。 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

次の識別子は、アドレス帳の Capone Profile セクション用で、複数の Exchange ([MultiEx](using-multiple-exchange-accounts.md)) メールボックスのサポートに使用され、[PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) プロパティが含まれます。このプロパティは [SetDefaultDir](iaddrbook-setdefaultdir.md) によって指定された既定のコンテナーを事実上無効にします。
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a>インターフェイス識別子

#### <a name="imapisync"></a>IMAPISync
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a>IMAPISyncProgressCallback
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a>IID_IContabAdmin
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a>IID_IMAPISECUREMESSAGE
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a>IID_IMAPIGetSession
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a>PST 上書きハンドラーのインターフェイス識別子

#### <a name="iidipstoverridereq"></a>IID_IPSTOVERRIDEREQ
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a>IID_IPSTOVERRIDE1
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a>関連項目

- [MAPI の追加について](about-mapi-additions.md) 
- [Outlook で使用される名前付きプロパティについて](about-named-properties-used-by-outlook.md)
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Exchange キャッシュ モードで同期を呼び出すことなく OST でメッセージを管理する](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

