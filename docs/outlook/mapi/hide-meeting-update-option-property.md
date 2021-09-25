---
title: 会議の更新オプションプロパティを非表示にする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ee97b6bde17a1129781de18e7d16d142d3b97193
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564345"
---
# <a name="hide-meeting-update-option-property"></a>会議の更新オプションプロパティを非表示にする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
追加または削除された出席者にのみ会議の更新プログラムを送信するオプションを非表示にします。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の場合に公開されます。  <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) オブジェクト  <br/> |
|作成者:  <br/> |ストア プロバイダー  <br/> |
|アクセス者:  <br/> |Outlookクライアント  <br/> |
|プロパティの種類:  <br/> |PT_BOOLEAN  <br/> |
|アクセスの種類:  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

ストア機能を提供するには、ストア プロバイダーが [IMAPIProp : IUnknown](imapipropiunknown.md) を実装し [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) 呼び出しに渡されるこれらのプロパティの有効なプロパティ タグを返す必要があります。 これらのプロパティのプロパティ タグが [IMAPIProp::GetProps](imapiprop-getprops.md)に渡される場合、ストア プロバイダーは正しいプロパティ値も返す必要があります。 ストア プロバイダーは [、HrGetOneProp](hrgetoneprop.md) と [HrSetOneProp](hrsetoneprop.md) を呼び出して、これらのプロパティを取得または設定できます。 
  
このプロパティの値を取得するには、まず [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) を使用してプロパティ タグを取得し [、IMAPIProp::GetProps](imapiprop-getprops.md) でこのプロパティ タグを指定して値を取得する必要があります。 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lppPropNames_ が指す [MAPINAMEID](mapinameid.md)構造体に次の値を指定します。
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"  <br/> |
   
サーバーを使用して会議の更新プログラムを送信するストア プロバイダーは、[出席者に更新プログラムを送信する] ダイアログ ボックス **を** 変更できます。 この機能は、サーバーが会議の更新プログラムを送信するときに、最初の会議出席依頼以降にユーザーが追加または削除した出席者をサーバーが知らないので便利です。 このプロパティが **true の場合**、[更新プログラムを追加または削除した出席者にのみ送信する] オプションは、[出席者に更新プログラムを送信する] ダイアログ ボックス **には** 表示されません。 
  
このプロパティは、2003 Service Pack 1 のバージョンOutlook 2003 Service Pack 1 より前Microsoft Office Outlook、または値が false の場合は無視 **されます**。
  

