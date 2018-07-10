---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1e0c099783b4d44b1aaf746b07c77981c135ca9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19799687"
---
# <a name="archivesourcesupportmask"></a>ArchiveSourceSupportMask

  
  
**適用されます**: Outlook 
  
Microsoft Office Outlook がストア内のフォルダーをスキャンし、自動的にアーカイブしてかどうかを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|公開されます。  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)オブジェクト  <br/> |
|によって作成されます。  <br/> |ストア プロバイダー  <br/> |
|によってアクセスします。  <br/> |Outlook およびその他のクライアント  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|アクセスの種類:  <br/> |読み取り専用または読み取り/書き込みによってストア プロバイダー  <br/> |
   
## <a name="remarks"></a>備考

ストア機能を提供するストア プロバイダーを実装する必要があります[IMAPIProp: IUnknown](imapipropiunknown.md) 、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)の呼び出しに渡されたこれらのプロパティのいずれかのプロパティの有効なタグを返すとします。 これらのプロパティのいずれかのプロパティ タグが[IMAPIProp::GetProps](imapiprop-getprops.md)に渡されると、ストア プロバイダーを使用、正しいプロパティ値を返す必要があります。 ストア プロバイダーには、取得、またはこれらのプロパティを設定するには、 [HrGetOneProp](hrgetoneprop.md)と[HrSetOneProp](hrsetoneprop.md)を呼び出すことができます。 
  
このプロパティの値を取得するには、クライアントはまず[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して、プロパティ タグを取得して、値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティのタグを指定する必要があります。 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の次の値を指定します。
  
|||
|:-----|:-----|
|lpGuid。  <br/> |PSETID_Common  <br/> |
|ulKind。  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName。  <br/> |L"ArchiveSourceSupportMask"  <br/> |
   
このプロパティは、Outlook がストア内のフォルダーをスキャンし、自動的にアーカイブしているかどうかを指定するのには、ストア プロバイダーを使用します。
  
既定では、このプロパティは、ストアは、Outlook は、ストア上のフォルダーをスキャンできることを意味では公開されません。 プロパティが公開されている場合、値は次のことです。
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

ASM_DEFAULT
  
- Outlook では、ストア上のフォルダーをスキャンできます。
    
ASM_DO_NOT_ARCHIVE
  
- Outlook では、ストア上のフォルダーをスキャンする必要があります。
    
ASM_CLIENT_DO_NOT_CHANGE
  
- ストア内のこのプロパティを変更するクライアントを許可しません。 定数**ASM_CLIENT_DO_NOT_CHANGE**は、将来の参照と、現在実装されていません注意してください。 ここでは、ストアは、このプロパティでストアから返される値をハードコーディングするで、このフラグを変更することからクライアントを防ぐことができます。 
    
