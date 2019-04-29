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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418093"
---
# <a name="archivesourcesupportmask"></a>ArchiveSourceSupportMask

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook がストア内のフォルダーをスキャンして、それらを自動的にアーカイブするかどうかを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|公開:  <br/> |[IMsgStore: imapiprop](imsgstoreimapiprop.md)オブジェクト  <br/> |
|作成者:  <br/> |ストアプロバイダー  <br/> |
|アクセス先:  <br/> |Outlook およびその他のクライアント  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|アクセスの種類:  <br/> |ストアプロバイダーに応じて読み取り専用または読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

ストアの機能を提供するには、ストアプロバイダーが[imapiprop: IUnknown](imapipropiunknown.md)を実装し、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)呼び出しに渡されるこれらのプロパティに対して有効なプロパティタグを返す必要があります。 これらのプロパティのいずれかのプロパティタグが[imapiprop:: GetProps](imapiprop-getprops.md)に渡されると、ストアプロバイダーは、適切なプロパティ値を返す必要があります。 ストアプロバイダーは、 [hrgetoneprop](hrgetoneprop.md)および[hrgetoneprop](hrsetoneprop.md)を呼び出して、これらのプロパティを取得または設定できます。 
  
このプロパティの値を取得するには、クライアントはまず[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を使用してプロパティタグを取得し、次に[imapiprop:: GetProps](imapiprop-getprops.md)でこのプロパティタグを指定して値を取得する必要があります。 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lpppropnames_でポイントされている[mapinameid](mapinameid.md)構造に次の値を指定します。
  
|||
|:-----|:-----|
|lpguid:  <br/> |PSETID_Common  <br/> |
|ulkind:  <br/> |MNID_STRING  <br/> |
|種類が lpwstrname:  <br/> |L "ArchiveSourceSupportMask"  <br/> |
   
このプロパティを使用すると、Outlook がストア内のフォルダーをスキャンして、それらを自動的にアーカイブするかどうかを指定できます。
  
既定では、このプロパティはストアに公開されていないため、Outlook はストアのフォルダーをスキャンできます。 プロパティが公開されている場合は、次の値を指定できます。
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

ASM_DEFAULT
  
- Outlook は、ストア上のフォルダーをスキャンできます。
    
ASM_DO_NOT_ARCHIVE
  
- Outlook は、ストア上のフォルダーをスキャンしません。
    
ASM_CLIENT_DO_NOT_CHANGE
  
- クライアントがストアでこのプロパティを変更できないようにします。 定数**ASM_CLIENT_DO_NOT_CHANGE**は将来の参照用であり、現在は実装されていないことに注意してください。 この時点で、ストアは、このプロパティに対してストアが返す値をハードコーディングすることにより、クライアントがこのフラグを変更できないようにすることができます。 
    

