---
title: サーバーフォルダーのサイズプロパティを表示する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337080"
---
# <a name="display-server-folder-sizes-property"></a>サーバーフォルダーのサイズプロパティを表示する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サーバー上の指定されたフォルダーのサイズが [Outlook**フォルダーサイズ**] ダイアログボックスに表示されます。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|公開:  <br/> |[IMsgStore: imapiprop](imsgstoreimapiprop.md)オブジェクト  <br/> |
|作成者:  <br/> |ストアプロバイダー  <br/> |
|アクセス先:  <br/> |Outlook およびその他のクライアント  <br/> |
|プロパティの種類:  <br/> |PT_BOOLEAN  <br/> |
|アクセスの種類:  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>解説

ストアの機能を提供するには、ストアプロバイダーが[imapiprop: IUnknown](imapipropiunknown.md)を実装し、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)呼び出しに渡されるこれらのプロパティに対して有効なプロパティタグを返す必要があります。 これらのプロパティのいずれかのプロパティタグが[imapiprop:: GetProps](imapiprop-getprops.md)に渡されると、ストアプロバイダーは、適切なプロパティ値を返す必要があります。 ストアプロバイダーは、 [hrgetoneprop](hrgetoneprop.md)および[hrgetoneprop](hrsetoneprop.md)を呼び出して、これらのプロパティを取得または設定できます。 
  
このプロパティの値を取得するには、クライアントはまず[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を使用してプロパティタグを取得し、次に[imapiprop:: GetProps](imapiprop-getprops.md)でこのプロパティタグを指定して値を取得する必要があります。 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lpppropnames_でポイントされている[mapinameid](mapinameid.md)構造に次の値を指定します。
  
|||
|:-----|:-----|
|lpguid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulkind:  <br/> |MNID_STRING  <br/> |
|種類が lpwstrname:  <br/> |L "urn: スキーマ-microsoft-com: office: outlook # serverfoldersizes"  <br/> |
   
このプロパティは、Microsoft Outlook 2003 Service Pack (SP) 1 でサポートされています。 outlook のバージョンが outlook 2003 SP 1 より前の場合、またはその値が**false**の場合、outlook はローカルストア上のフォルダーのサイズのみを表示します。 outlook 2003 SP 1 を使用するストアにこのプロパティが設定されている場合、outlook はサーバー上の指定された各フォルダーとローカルドライブのサイズを照会します。 
  
サーバー上のフォルダーサイズを照会するには、Outlook は[IMsgStore:: openentry](imsgstore-openentry.md)を使用してストアのフォルダーを開き、フラグ**MAPI_NO_CACHE**を渡してから、 **PR_MESSAGE_SIZE_EXTENDED**に対するクエリを実行します。 その後、ストアプロバイダーは、サーバー上のフォルダーサイズを返す必要があります。
  
ローカルドライブのフォルダーのサイズを照会するには、 **MAPI_NO_CACHE**フラグを指定せずにフォルダーを開きます。 その後、 **PR_MESSAGE_SIZE_EXTENDED**に対するクエリを行います。ストアプロバイダーは、ローカルドライブ上の指定されたフォルダーのサイズを返す必要があります。
  
このプロパティセットを使用すると、ストアのコンテンツをサーバーに同期するストアプロバイダーは、Outlook の [**フォルダーサイズ**] ダイアログボックスで、サーバー上のフォルダーサイズデータを表示できます。 その後、ユーザーは現在のサーバー記憶域の使用状況をサーバークォータと比較できます。 
  

