---
title: ストアの種類をプライベート プロパティにする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428544"
---
# <a name="make-store-type-private-property"></a>ストアの種類をプライベート プロパティにする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セカンダリ ストアをプライベートとして扱います。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の場合に公開されます。  <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) オブジェクト  <br/> |
|作成者:  <br/> |ストア プロバイダー  <br/> |
|アクセス者:  <br/> |Outlookクライアント  <br/> |
|プロパティの種類:  <br/> |PT_BOOLEAN  <br/> |
|アクセスの種類:  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

ストア機能を提供するには、ストア プロバイダーが [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) を実装し [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) 呼び出しに渡されるこれらのプロパティの有効なプロパティ タグを返す必要があります。 これらのプロパティのプロパティ タグが [IMAPIProp::GetProps](imapiprop-getprops.md)に渡される場合、ストア プロバイダーは正しいプロパティ値も返す必要があります。 ストア プロバイダーは [、HrGetOneProp](hrgetoneprop.md) と [HrSetOneProp](hrsetoneprop.md) を呼び出して、これらのプロパティを取得または設定できます。 
  
このプロパティの値を取得するには、まず [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) を使用してプロパティ タグを取得し [、IMAPIProp::GetProps](imapiprop-getprops.md) でこのプロパティ タグを指定して値を取得する必要があります。 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lppPropNames_ が指す [MAPINAMEID](mapinameid.md)構造体に次の値を指定します。
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"  <br/> |
   
ストア プロバイダーは、このプロパティを使用して、Outlookセカンダリ ストアの場合にプライベートとして扱う必要があります。 
  
既定では、Outlookは代理ストアと同じ方法でセカンダリ ストアを扱い、セカンダリ ストア内のアイテムは、ユーザーがプライベートとして特別にマークした場合にのみプライベートになります。 このプロパティが **true の場合**、セカンダリ ストアから削除されたアイテムは、プライマリ ストアの **[削除** 済みアイテム] フォルダーに移動されます。 プライベートとマークされたアイテムは表示されません。 下書きは、プライマリ ストアの下書きフォルダーに保存されます。 
  
このプロパティは、2003 Service Pack 1 のバージョンOutlook 2003 Service Pack 1 より前Microsoft Office Outlook、または値が false の場合は無視 **されます**。
  

