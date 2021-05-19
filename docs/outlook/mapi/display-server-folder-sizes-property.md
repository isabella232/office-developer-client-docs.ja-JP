---
title: '[サーバー フォルダーサイズの表示] プロパティ'
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434551"
---
# <a name="display-server-folder-sizes-property"></a>[サーバー フォルダーサイズの表示] プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サーバー上の指定したフォルダーのサイズを [フォルダー のサイズ] ダイアログ ボックスOutlook **表示** します。 
  
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
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"  <br/> |
   
このプロパティは、Microsoft Outlook 2003 Service Pack (SP) 1 でサポートされています。 Outlook のバージョンが Outlook 2003 SP 1 より前の場合、または値が **false** の場合、Outlook はローカル ストア上のフォルダーのサイズのみを表示します。 Outlook 2003 SP 1 を使用するストアでこのプロパティが設定されている場合、Outlook はサーバー上の指定された各フォルダーとローカル ドライブのサイズを照会します。 
  
サーバー上のフォルダー サイズを照会するために、Outlook は [IMsgStore::OpenEntry](imsgstore-openentry.md)を使用してストア上のフォルダーを開き、フラグ **MAPI_NO_CACHE** を渡し、PR_MESSAGE_SIZE_EXTENDED を **照会します**。 ストア プロバイダーは、サーバー上のフォルダー サイズを返す必要があります。
  
ローカル ドライブ上のフォルダーのサイズを照会するには、Outlookフラグなしでフォルダー **MAPI_NO_CACHE** します。 次に、クエリを実行 **PR_MESSAGE_SIZE_EXTENDED。** ストア プロバイダーは、ローカル ドライブ上の指定したフォルダーのサイズを返す必要があります。
  
このプロパティセットを使用すると、ストアの内容をサーバーに同期するストア プロバイダーは、[フォルダー サイズ] ダイアログ ボックスの **[Outlook]** にフォルダー サイズデータを表示できます。 その後、ユーザーは現在のサーバー ストレージ使用量とサーバー クォータを比較できます。 
  

