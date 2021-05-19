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
  
ストア内のMicrosoft Office Outlookをスキャンして自動的にアーカイブするかどうかを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の場合に公開されます。  <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) オブジェクト  <br/> |
|作成者:  <br/> |ストア プロバイダー  <br/> |
|アクセス者:  <br/> |Outlookクライアント  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|アクセスの種類:  <br/> |ストア プロバイダーに応じて読み取り専用または読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

ストア機能を提供するには、ストア プロバイダーが [IMAPIProp : IUnknown](imapipropiunknown.md) を実装し [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) 呼び出しに渡されるこれらのプロパティの有効なプロパティ タグを返す必要があります。 これらのプロパティのプロパティ タグが [IMAPIProp::GetProps](imapiprop-getprops.md)に渡される場合、ストア プロバイダーは正しいプロパティ値も返す必要があります。 ストア プロバイダーは [、HrGetOneProp](hrgetoneprop.md) と [HrSetOneProp](hrsetoneprop.md) を呼び出して、これらのプロパティを取得または設定できます。 
  
このプロパティの値を取得するには、まず [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) を使用してプロパティ タグを取得し [、IMAPIProp::GetProps](imapiprop-getprops.md) でこのプロパティ タグを指定して値を取得する必要があります。 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lppPropNames_ が指す [MAPINAMEID](mapinameid.md)構造体に次の値を指定します。
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"ArchiveSourceSupportMask"  <br/> |
   
このプロパティを使用すると、ストア プロバイダーは、Outlookフォルダーをスキャンして自動的にアーカイブするかどうかを指定できます。
  
既定では、このプロパティはストアで公開されません。つまり、Outlookフォルダーをスキャンできます。 プロパティが公開されている場合は、次の値を使用できます。
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

ASM_DEFAULT
  
- Outlookストア上のフォルダーをスキャンできます。
    
ASM_DO_NOT_ARCHIVE
  
- Outlookフォルダーをスキャンしない必要があります。
    
ASM_CLIENT_DO_NOT_CHANGE
  
- クライアントがストアでこのプロパティを変更を許可しない。 定数の値は **ASM_CLIENT_DO_NOT_CHANGE** 参照用であり、現在実装されていません。 今のところ、ストアは、このプロパティに対してストアが返す値をハードコードすることで、クライアントがこのフラグを変更できません。 
    

