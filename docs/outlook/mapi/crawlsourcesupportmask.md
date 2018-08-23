---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cc8ff946081fb7817f0f6018acefbe31293a13a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581777"
---
# <a name="crawlsourcesupportmask"></a>CrawlSourceSupportMask

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
Microsoft Office Outlook では、ナビゲーション ウィンドウに表示する起動時に、連絡先、カレンダー、およびタスクのフォルダーを含むストア内のフォルダーをスキャンするかどうかを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|公開されます。  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)オブジェクト  <br/> |
|によって作成されます。  <br/> |ストア プロバイダー  <br/> |
|によってアクセスします。  <br/> |Outlook およびその他のクライアント  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|アクセスの種類:  <br/> |読み取り専用または読み取り/書き込みによってストア プロバイダー  <br/> |
   
## <a name="remarks"></a>注釈

ストア機能を提供するストア プロバイダーを実装する必要があります[IMAPIProp: IUnknown](imapipropiunknown.md) 、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)の呼び出しに渡されたこれらのプロパティのいずれかのプロパティの有効なタグを返すとします。 これらのプロパティのいずれかのプロパティ タグが[IMAPIProp::GetProps](imapiprop-getprops.md)に渡されると、ストア プロバイダーを使用、正しいプロパティ値を返す必要があります。 ストア プロバイダーには、取得、またはこれらのプロパティを設定するには、 [HrGetOneProp](hrgetoneprop.md)と[HrSetOneProp](hrsetoneprop.md)を呼び出すことができます。 
  
このプロパティの値を取得するには、クライアントはまず[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して、プロパティ タグを取得して、値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティのタグを指定する必要があります。 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の次の値を指定します。
  
|||
|:-----|:-----|
|lpGuid。  <br/> |PSETID_Common  <br/> |
|ulKind。  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName。  <br/> |L"CrawlSourceSupportMask"  <br/> |
   
このプロパティは、Outlook がストア内のさまざまなフォルダーをスキャンするかどうかを指定するのには、ストア プロバイダーの方法を提供します。 Outlook は、**ナビゲーション**ウィンドウを設定するのには開かれている各ストアで既存のフォルダーをスキャンする場合の起動時に使用されます。Outlook は、スキャンを開始する前に存在し、ストアでは、このプロパティの値をチェックします。 
  
既定では、このプロパティは、ストアは、Outlook は、ストア上のフォルダーをスキャンできることを意味では公開されません。 プロパティが公開されている場合、値は次のことです。
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

CSM_DEFAULT
  
- Outlook では、ストア上のフォルダーをスキャンできます。
    
CSM_DO_NOT_CRAWL
  
- Outlook では、ストア上のフォルダーをスキャンする必要があります。
    
CSM_CLIENT_DO_NOT_CHANGE
  
- ストア内のこのプロパティを変更するクライアントを許可しません。 定数**CSM_CLIENT_DO_NOT_CHANGE**は、将来の参照と、現在実装されていません注意してください。 ここでは、ストアは、このプロパティでストアから返される値をハードコーディングするで、このフラグを変更することからクライアントを防ぐことができます。 
    

