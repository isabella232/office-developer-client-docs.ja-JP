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
# <a name="mapi-constants"></a>MAPI の定数

**適用対象**: Outlook 
  
このトピックには、定数の定義、MAPI インターフェイスの宣言、および MAPI Api で使用されるクラスとインタ フェースの識別子が含まれています。
  
## <a name="class-and-interface-identifiers"></a>クラス識別子とインターフェイス識別子

DEFINE_GUID マクロを Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル guiddef.h に定義されているを使用して、特に明記しない限りの値は、シンボル名のグローバル一意識別子 (GUID) を関連付けます。
  
## <a name="attachment-security-conversion-api"></a>添付ファイル セキュリティの変換 API

ここには、添付ファイル セキュリティ API の定数の定義およびインタ フェース識別子が含まれています。
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

純粋仮想関数**[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)** を定義するのにには、Windows SDK のヘッダー ファイル mapidefs.h に定義されている MAPIMETHOD マクロを使用します。 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

**[IAttachmentSecurity](iattachmentsecurityiunknown.md)** の仮想メソッド テーブルを定義するのにには、Windows SDK のヘッダー ファイル mapidefs.h に定義されている DECLARE_MAPI_INTERFACE_ マクロを使用します。 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a>MAPI から MIME への変換 API

このセクションには、MAPI から MIME 変換 API の定数の定義、クラス識別子とインターフェイス識別子が含まれています。
  
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
|E_INVALIDARG  <br/> | *Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル winerror.h で定義されています。*  <br/> |
   
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

## <a name="offline-state-api"></a>オフライン状態の API

このセクションには、オフライン状態 API の定数の定義、クラス識別子とインターフェイス識別子が含まれています。
  
### <a name="constants"></a>定数

|||
|:-----|:-----|
|E_INVALIDARG  <br/> | *Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル winerror.h で定義されています。*  <br/> |
|E_NOINTERFACE  <br/> | *Windows (SDK) のヘッダー ファイル winerror.h で定義されています。*  <br/> |
|MAPIOFFLINE_ADVISE_DEFAULT  <br/> |(ULONG) 0  <br/> |
|MAPIOFFLINE_UNADVISE_DEFAULT  <br/> |(ULONG) 0  <br/> |
|MAPIOFFLINE_ADVISE_TYPE_STATECHANGE  <br/> |1  <br/> |
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |0x1  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |0x2  <br/> |
|MAPIOFFLINE_FLAG_BLOCK  <br/> |0x00002000  <br/> |
|MAPIOFFLINE_FLAG_DEFAULT  <br/> |0x00000000  <br/> |
|MAPIOFFLINE_STATE_ALL  <br/> |0x003f037f  <br/> |
|**オンラインあるいはオフライン** <br/> ||
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

## <a name="outlook-named-properties"></a>Outlook は名前付きプロパティ

このセクションには、名前付きプロパティの定数の定義とその名前空間、およびその他の関連する定数が含まれています。
  
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

次のグローバル一意識別子 (Guid) は、名前付きプロパティの名前空間を表します。
  
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

PSETID の定義は、MAPI ストアを参照してください。
  
### <a name="other-constants"></a>他の定数

|||
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0xD000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x2000000  <br/> |
|MNID_ID  <br/> | *ヘッダー ファイルの mapidefs.h で定義します。*  <br/> |
|MNID_STRING  <br/> | *ヘッダー ファイルの mapidefs.h で定義します。*  <br/> |
|mtgNone  <br/> |0x0  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |
|mtgFullUpdate  <br/> |0x00010000  <br/> |
|mtgInfoUpdate  <br/> |0x00020000  <br/> |
|mtgOutofDate  <br/> |0x00080000  <br/> |
|mtgDelegated  <br/> |0x00100000  <br/> |
   
## <a name="replication-api"></a>レプリケーション API

このセクションには、レプリケーション API の定数の定義、MAPI インターフェイスの宣言、およびクラス識別子とインターフェイス識別子が含まれています。
  
### <a name="constants"></a>定数

MAPI サービス プロバイダーを識別する[MAPIUID](mapiuid.md)構造体は次のとおりです。 
  
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
|MDB_OST_LOGON_UNICODE  <br/> |((ULONG) 0X00000800)  <br/> |
|MDB_OST_LOGON_ANSI  <br/> |((ULONG) 0X00001000)  <br/> |
|SHOW_SOFT_DELETES  <br/> |((ULONG) 0X00000002)  <br/> |
|SS_ACTIVE  <br/> |0  <br/> |
|SS_SUSPENDED  <br/> |1  <br/> |
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
   
### <a name="interface-declarations"></a>インターフェイスの宣言

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

[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)、 [IMAPISession::OpenEntry](imapisession-openentry.md)、または[IMsgStore::OpenEntry](imsgstore-openentry.md)を開き、それぞれのフォルダー オブジェクトとメッセージ オブジェクトのいずれかのプロバイダー チェックを無視して次の 2 つのインターフェイス識別子を使用します。 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a>MAPI ストア

このセクションには、定数の定義が含まれています、インタ フェース識別子によって使用 Api インターフェイス MAPI ストアを持つ。
  
### <a name="constants"></a>定数

||||
|:-----|:-----|:-----|
|fnevIndexing  <br/> |((ULONG) 0X00010000)  <br/> |ストア プロバイダーは、オブジェクトがインデックス作成の準備が完了であることをインデクサーに通知する**[通知](notification.md)** の構造体の**ulEventType**メンバーに**fnevIndexing**を指定できます。 **通知**の構造体のメンバー**情報**には、 **[EXTENDED_NOTIFICATION](extended_notification.md)** 構造体が含まれています。  <br/> |
|FS_NONE  <br/> |0x00  <br/> |クライアントは、返されるビットマスクの**[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** とチェックを呼び出すことができます。 **FS_NONE**は、フォルダーを共有するサポートしていないことを示します。  <br/> |
|FS_SUPPORTS_SHARING  <br/> |0x01  <br/> |クライアントは、返されるビットマスクの**IFolderSupport::GetSupportMask**とチェックを呼び出すことができます。 **FS_SUPPORTS_SHARING**では、共有フォルダーをサポートしていることを示します。  <br/> |
|INDEXING_SEARCH_OWNER  <br/> |((ULONG) 0X00000001)  <br/> |させようとして、通知オブジェクトは、インデックス作成の準備ができて、インデクサーのプロセスを識別します。  <br/> |
|MNID_ID  <br/> |Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル mapidefs.h に定義されています。  <br/> |**UlKind** 、 **[MAPINAMEID](mapinameid.md)** 構造体のフィールドの値です。  <br/> |
|MNID_STRING  <br/> |Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル mapidefs.h で定義します。  <br/> |**UlKind** 、 **[MAPINAMEID](mapinameid.md)** 構造体のフィールドの値です。  <br/> |
|MSCAP_RES_ANNOTATION  <br/> |((ULONG) 0X00000001)  <br/> |クライアントは、 **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)** の*mscapSelector*で**MSCAP_SEL_RESTRICTION**を指定する場合**GetCapabilities**は、ストアは、制限の中で無効なパラメーターを無視する場合にこの値を返すことができます。  <br/> |
|MSCAP_SECURE_FOLDER_HOMEPAGES  <br/> |((ULONG) 0X00000020)  <br/> |クライアントは、 **IMSCapabilities::GetCapabilities**の*mscapSelector*で**MSCAP_SEL_FOLDER**を指定した場合、 **GetCapabilities**はストアがフォルダーのホーム ページをサポートする既定以外のストアである場合にこの値を返すことができます。  <br/> |
|STORE_PUSHER_OK  <br/> |((ULONG) 0X00800000)  <br/> |クライアントは、メッセージ ・ ストアの特性を決定する**[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** プロパティを取得できます。 ストア プロバイダーは、ビットマスク内の**STORE_PUSHER_OK**フラグを設定、MAPI プロトコル ハンドラーはストアをクロールしないと、ストアは、メッセージのインデックスを作成するのにはインデクサーに通知を使用して、変更をプッシュすることを意味します。  <br/> |
   
### <a name="definitions-for-namespaces"></a>名前空間の定義

次のグローバル一意識別子 (Guid) は、名前付きプロパティの名前空間を表します。 MAPI プロトコル ハンドラー (PH) では、インデックスを作成、読み取り専用として記載されています。
  
> [!CAUTION]
> 作成または項目を変更する名前付きプロパティを使用してくださいできません。 
  
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

使用して、`DEFINE_OLEGUID`の値で、次の GUID のシンボリック名を関連付けるには、Windows SDK ヘッダー ファイル guiddef.h に定義されているマクロ。 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a>MAPI アドレス帳の定数

このセクションには、MAPI アドレス帳の定数の定義が含まれています。
  
### <a name="constants"></a>定数

||||
|:-----|:-----|:-----|
|CONTAB_ROOT  <br/> |((ULONG) 0X00000001)  <br/> |MAPI アドレス帳オブジェクトのルート フォルダーです。  <br/> |
|CONTAB_SUBROOT  <br/> |((ULONG) 0X00000002)  <br/> |MAPI アドレス帳のオブジェクトのルート フォルダー内に含まれるサブフォルダー。  <br/> |
|CONTAB_CONTAINER  <br/> |((ULONG) 0X00000003)  <br/> |�A�h���X���̃R���e�i�[ �I�u�W�F�N�g�ł��B  <br/> |
|CONTAB_USER  <br/> |((ULONG) 0X00000004)  <br/> |���b�Z�[�W���O ���[�U�[ �I�u�W�F�N�g�ł��B  <br/> |
|CONTAB_DISTLIST  <br/> |((ULONG) 0X00000005)  <br/> |�z�z���X�g �I�u�W�F�N�g�ł��B  <br/> |
   
## <a name="additional-mapi-constants"></a>追加の MAPI 定数

このセクションには、エラー コード、および公開され文書化されていない MAPI Api で使用されるインターフェイス識別子を含む定数の定義が含まれています。
  
||||
|:-----|:-----|:-----|
|DIALOG_MODAL  <br/> |((ULONG) 0X00000001)  <br/> |クライアントが[IAddrBook::Details](iaddrbook-details.md)メソッドを呼び出すと、クライアントは、 _ulFlags_パラメーターを特定のアドレス帳のエントリに関する詳細を表示するモーダル ダイアログ ボックスを表示するに**DIALOG_MODAL**フラグを設定する必要があります。 この定数は、mapidefs.h で定義されます。  <br/> |
|ITEMPROC_FORCE  <br/> |0x00000800  <br/> |Outlook 2007 では、ラップされた PST ストアがルールにあり、MAPI クライアントは、新しいメッセージの通知を受け取る前に新しいメッセージ スパム フィルター処理します。 プロバイダーまたは PST ストアで新しいメッセージを作成するのには、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを使用してクライアントは、 _ulFlags_メソッドのパラメーターに、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md) PST に示すために**ITEMPROC_FORCE**フラグを設定する必要があります。ストアは、メッセージの対象とする規則をストアが、新しいメッセージの到着をリッスンしているすべてのクライアントに通知する前に処理します。 Exchange Server がサーバー上のメッセージのルールを処理するために Microsoft Exchange Server ではないサーバー上で作成された新しいメッセージだけを処理するこのような規則が適用されることに注意してください。 したがって、プロバイダーまたはメッセージを作成するクライアントは、 **NON_EMS_XP_SAVE**サーバーが Exchange サーバーではないことを示すとの組み合わせでこのフラグを渡す必要があります。  <br/> |
| MAPI_BG_SESSION  <br/> |0x00200000  <br/> |クライアントは、セッションにログオンし、バック グラウンドで任意の操作を実行するには、 _flFlags_パラメーターで**MAPI_BG_SESSION**フラグを設定、 [MAPILogonEx](mapilogonex.md)関数を呼び出すことができます。 一般に、クライアントがバック グラウンド スレッドかフォア グラウンド スレッドに目障りではない方法で別のプロセスでの処理を実行しようとすると場合、は、 **MAPI_BG_SESSION**フラグを使用して[MAPILogonEx](mapilogonex.md)を呼び出す必要があります。 これが使用されている例は、バック グラウンドのアクセス権の種類の個人用フォルダー ファイル (PST) を開く、インデックス エンジンなど、クライアント アプリケーションです。  <br/> |
|MAPI_CACHE_ONLY  <br/> |0x00004000  <br/> |クライアントは、 _ulFlags_パラメーター エントリをアドレス帳を開くと、キャッシュからのみ、その後にアクセスするために**MAPI_CACHE_ONLY**フラグを設定、[アドレス帳コンテナー](iaddrbook-openentry.md)のメソッドを呼び出すことができます。 これが使用されている例は、Exchange キャッシュ モードでグローバル アドレス一覧を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスしようとしているクライアント アプリケーションです。  <br/> |
|MAPI_DIALOG_MODELESS  <br/> |0x0000000C  <br/> |_UlFlags_パラメーターで既定の電子メール アプリケーションにモードレス ダイアログ ボックスが表示されることを指定するには、簡易 MAPI MAPISendMail 関数には、この値を渡すことができます。 このフラグも MAPI_DIALOG (0x00000008) が設定されている場合、ダイアログ ボックスは表示されません。  <br/> |
|MAPI_NO_CACHE  <br/> |0x00000200  <br/> |Microsoft Office Outlook が Exchange キャッシュ モードでは、ストアは、キャッシュ モードで開かれていた場合は、クライアントまたはサービス プロバイダーが[IMsgStore::OpenEntry](imsgstore-openentry.md)、 **MAPI_NO_CACHE**フラグを設定して、 _ulFlags_に渡すパラメーターでアイテムを開くを呼び出すことができますか、リモート ストア上のフォルダーです。 場合は、メッセージ ストアを開くには、リモート サーバー上で**MDB_ONLINE**フラグを使用して、必要はありません**MAPI_NO_CACHE**フラグを使用するに注意してください。  <br/> |
|MAPI_UNICODE  <br/> |0x80000000  <br/> |クライアントまたはサービス プロバイダーは、Unicode の .msg ファイルを作成する_ulFlags_パラメーターに**MAPI_UNICODE**フラグを設定する、 [OpenIMsgOnIStg](openimsgonistg.md)関数を呼び出すことができます。 結果[IMessage: IMAPIProp](imessageimapiprop.md)ファイルは、 [PidTagStoreSupportMask の標準的なプロパティ](pidtagstoresupportmask-canonical-property.md)に**STORE_UNICODE_OK**を示しています、Unicode プロパティをサポートしています。 この定数は、mapidefs.h で定義されます。  <br/> |
|MDB_ONLINE  <br/> |0x00000100  <br/> |Outlook が Exchange キャッシュ モードの場合は、クライアントまたはサービス プロバイダー メソッドを呼び出して、 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) 、ローカル メッセージ ストアへの接続をオーバーライドし、開く_ulFlags_パラメーターで**MDB_ONLINE**フラグを設定します。リモート サーバー上のストアです。 開くことができない、Exchange ストアをキャッシュ モードと非キャッシュ モードで新しい MAPI セッションに同時に注意してください。 キャッシュされたメッセージ ストアを既に開いている場合、このフラグで開き、またはこのフラグを使用してリモート サーバー上の Exchange ストアを開く新しい MAPI セッションを開始する前にストアを閉じる必要がありますか。  <br/> |
|NON_EMS_XP_SAVE  <br/> |0x00001000  <br/> |クライアントは、Exchange サーバーからメッセージが配信されていないことを示すために_ulFlags_パラメーターに**NON_EMS_XP_SAVE**フラグを設定する、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すことができます。 このフラグは組み合わせて使用する_ulFlags_パラメーターに**ITEMPROC_FORCE**フラグを使用してを示すメッセージが pst ファイルの前に処理ルールの対象とする PST ストアにストアに通知の到着をリッスンしているクライアントはすべて、メッセージ。 これは、ルールを (場合に Exchange サーバーは既に処理が、メッセージのルール)、Exchange サーバーではないサーバー上の[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)で作成された新しいメッセージに適用されますのみを処理します。  <br/> |
|SPAMFILTER_ONSAVE  <br/> |0x00000080  <br/> |クライアントは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)、 **SPAMFILTER_ONSAVE**フラグを設定して迷惑メールが保存されるメッセージのフィルタ リングを有効にする_ulFlags_パラメーターを呼び出すことができます。 スパムのフィルタ リングのサポートは、送信者の電子メール アドレスの種類は、簡易メール転送プロトコル (SMTP)、メッセージは個人用フォルダー ファイル (PST) のストアに保存されている場合にのみ使用できます。  <br/> |
|STORE_ITEMPROC  <br/> |0x00200000  <br/> |ラップされた PST ストアの[PidTagStoreSupportMask の標準的なプロパティ](pidtagstoresupportmask-canonical-property.md)で、このフラグが設定されている場合は、ストアでは、新しいメッセージが到着すると、ストアには、ルールを個別に、メッセージに適用されるスパムのフィルタ リングを示します。 ストアは、 [IMAPISupport::Notify](imapisupport-notify.md)、 **fnevNewMail**をパラメーターとして渡される[通知](notification.md)の構造体に設定し、リッスンしているクライアントに新しいメッセージの詳細を渡すことを呼び出します。 その後、リッスンしているクライアントでは、通知を受信すると、メッセージのルールは処理されません。  <br/> |
|STORE_UNICODE_OK  <br/> |0x00040000  <br/> |[PidTagStoreSupportMask の標準的なプロパティ](pidtagstoresupportmask-canonical-property.md)には、このフラグが含まれる場合、は、ストアが Unicode のストレージをサポートしていることを示します。 クライアントは Unicode 情報をストアに保存するかを要求するかを決定するフラグの有無を確認できます。  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a>フォルダー内のアイテムをアーカイブするための定義

次の定数の定義は、 [PidTagAgingGranularity の標準的なプロパティ](pidtagaginggranularity-canonical-property.md)を設定するために使用する値です。
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a>リモート オブジェクトを表示するための定義

次の定数とマクロの定義は、リモート オブジェクトを表示するのには。 詳細については、 [PidTagDisplayTypeEx の標準的なプロパティ](pidtagdisplaytypeex-canonical-property.md)を参照してください。
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a>エラー コードを格納する Exchange のアドレス帳とメッセージの定義

次には、再接続の機能が搭載されている Exchange のアドレス帳とメッセージ ・ ストアのエラー コード定義が含まれています。 最後の呼び出しの切断されたグローバル カタログ (GC) に**MAPI_E_END_OF_SESSION**エラーを再試行する必要があります。 
  
Outlook の MAPI サポートへの再接続 GC サーバーに特別な再構成がその他のエラー コードをクライアントに返すことができます。
  
||||
|:-----|:-----|:-----|
|MAPI_E_END_OF_SESSION  <br/> |0x80040200  <br/> |接続が切断されたときに返されます。  <br/> |
|MAPI_E_RECONNECTED  <br/> |0x80040125  <br/> |リモート プロシージャ コール (RPC) 接続のトークンが最新でない場合に返されます。 現在のトランザクションのトークンとは異なる場合ことを意味する接続のトークンが再接続、 **MAPI_E_RECONNECTED**が返されすることができますので**MAPI_E_END_OF_SESSION**と同じに扱われます。 呼び出しを再試行する必要があります。  <br/> |
|MAPI_E_OFFLINE  <br/> |0x80040126  <br/> |接続がオフラインのときに返されます。 つまり、通常サーバーの障害またはネットワーク接続が失われるなど、環境に何かが発生したことです。 このエラーは、キャッシュ モードを使用する場合に発生する可能性があります、プロファイル、およびサーバーと通信するためにキャッシュをバイパスしようとしています。 キャッシュは最初にサーバーへの接続を確立することはありませんでした、 **MAPI_E_OFFLINE**の表面に使用可能性があります、オフライン状態である可能性があります。  <br/> |
   
上記の 2 つのエラーのどちらも表示されますすべてのシナリオで表示される場所は多くの場合を適用します。 ほとんどの場合、 **MAPI\_E_NETWORK_ERROR** **MAPI_E_CALL_FAILED**が返されますか。 [MAPI クライアントの Microsoft Exchange Server と共同作業データ オブジェクト 1.2.1](http://support.microsoft.com/kb/171440)のダウンロードを使用しても表示されます。 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a>Exchange Server メールボックスの定義がキャッシュ モードのクォータ

次の定数の定義は、Microsoft Outlook 2010 で使用され、Exchange を設定するのには、Microsoft Outlook 2013 のキャッシュ モード プロファイル クォータは、それ以外の場合、オンライン プロファイルでのみ使用可能な Exchange メールボックスのクォータに相当します。
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

これらのプロパティは、通信のオンラインのプロパティにマップされ、キロバイト単位で同じ値が含まれています。 PR_QUOTA_WARNING は、PR_STORAGE_QUOTA_LIMIT へ PR_QUOTA_PROHIBIT_SEND_QUOTA、PR_QUOTA_SEND と PR_PROHIBIT_RECEIVE_QUOTA を PR_QUOTA_RECEIVE にマップされます。
  
### <a name="definitions-for-message-format"></a>メッセージ形式の定義

次の定数の定義は、 [PidTagMessageEditorFormat の標準的なプロパティ](pidtagmessageeditorformat-canonical-property.md)を設定するために使用する値です。
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a>HTTP 経由で RPC を使用するための定義

プロパティを設定するのにはフラグとして使用される定数の定義は[PidTagRpcOverHttpFlags の標準的なプロパティ](pidtagrpcoverhttpflags-canonical-property.md)のトピックを参照してください。 
  
プロパティを設定するために使用する定数の定義は[PidTagRpcOverHttpProxyAuthScheme の標準的なプロパティ](pidtagrpcoverhttpproxyauthscheme-canonical-property.md)のトピックを参照してください。 
  
### <a name="identifiers"></a>識別子

使用して、`DEFINE_OLEGUID`の値は次の GUID のシンボリック名を関連付けるには Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル guiddef.h に定義されているマクロ。 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

次の識別子は、複数の ([MultiEx](using-multiple-exchange-accounts.md)) の Exchange メールボックスをサポートするためを効果的に既定値を無効にする[PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)プロパティが含まれているアドレス帳の Capone プロファイル セクションのします。[SetDefaultDir](iaddrbook-setdefaultdir.md)で指定されたコンテナーです。
  
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

### <a name="pst-override-handler-interface-identifiers"></a>PST のオーバーライドのハンドラーのインターフェイス識別子

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

