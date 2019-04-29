---
title: ストアの種類をプライベートプロパティに設定する
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
# <a name="make-store-type-private-property"></a>ストアの種類をプライベートプロパティに設定する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セカンダリストアをプライベートとして扱います。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|公開:  <br/> |[IMsgStore: imapiprop](imsgstoreimapiprop.md)オブジェクト  <br/> |
|作成者:  <br/> |ストアプロバイダー  <br/> |
|アクセス先:  <br/> |Outlook およびその他のクライアント  <br/> |
|プロパティの種類:  <br/> |PT_BOOLEAN  <br/> |
|アクセスの種類:  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

ストアの機能を提供するには、ストアプロバイダーが[IMsgStore: imapiprop](imsgstoreimapiprop.md)を実装し、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)呼び出しに渡されるこれらのプロパティに対して有効なプロパティタグを返す必要があります。 これらのプロパティのいずれかのプロパティタグが[imapiprop:: GetProps](imapiprop-getprops.md)に渡されると、ストアプロバイダーは、適切なプロパティ値を返す必要があります。 ストアプロバイダーは、 [hrgetoneprop](hrgetoneprop.md)および[hrgetoneprop](hrsetoneprop.md)を呼び出して、これらのプロパティを取得または設定できます。 
  
このプロパティの値を取得するには、クライアントはまず[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を使用してプロパティタグを取得し、次に[imapiprop:: GetProps](imapiprop-getprops.md)でこのプロパティタグを指定して値を取得する必要があります。 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lpppropnames_でポイントされている[mapinameid](mapinameid.md)構造に次の値を指定します。
  
|||
|:-----|:-----|
|lpguid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulkind:  <br/> |MNID_STRING  <br/> |
|種類が lpwstrname:  <br/> |L "urn: スキーマ-microsoft-com: office: outlook # storetypeprivate"  <br/> |
   
ストアプロバイダーは、このプロパティを使用して、ユーザーのセカンダリストアである場合に、Outlook でこのプロパティをプライベートとして扱うことができます。 
  
既定では、Outlook は代理ストアと同じ方法でセカンダリストアを処理し、セカンダリストア内のアイテムはプライベートとしてマークされている場合にのみプライベートとして扱われます。 このプロパティが**true**の場合、セカンダリストアから削除されたアイテムは、プライマリストアの [**削除済みアイテム**] フォルダーに移動されます。 親展とマークされたアイテムは表示されません。 下書きは、プライマリストアの [下書き] フォルダーに保存されます。 
  
outlook のバージョンが Microsoft Office Outlook 2003 Service Pack 1 より前の場合、またはその値が**false**の場合、このプロパティは無視されます。
  

