---
title: サーバー フォルダーのサイズ プロパティの表示
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1ddf4501918d598169a3a74fd1c8d2ac38499cd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799929"
---
# <a name="display-server-folder-sizes-property"></a>サーバー フォルダーのサイズ プロパティの表示

  
  
**適用されます**: Outlook 
  
Outlook の **[フォルダー サイズ**] ダイアログ ボックスでサーバー上の指定したフォルダーのサイズを表示します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|公開されます。  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)オブジェクト  <br/> |
|によって作成されます。  <br/> |ストア プロバイダー  <br/> |
|によってアクセスします。  <br/> |Outlook およびその他のクライアント  <br/> |
|プロパティの種類:  <br/> |PT_BOOLEAN  <br/> |
|アクセスの種類:  <br/> |値の取得および設定が可能です。  <br/> |
   
## <a name="remarks"></a>備考

ストア機能を提供するストア プロバイダーを実装する必要があります[IMAPIProp: IUnknown](imapipropiunknown.md) 、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)の呼び出しに渡されたこれらのプロパティのいずれかのプロパティの有効なタグを返すとします。 これらのプロパティのいずれかのプロパティ タグが[IMAPIProp::GetProps](imapiprop-getprops.md)に渡されると、ストア プロバイダーを使用、正しいプロパティ値を返す必要があります。 ストア プロバイダーには、取得、またはこれらのプロパティを設定するには、 [HrGetOneProp](hrgetoneprop.md)と[HrSetOneProp](hrsetoneprop.md)を呼び出すことができます。 
  
このプロパティの値を取得するには、クライアントはまず[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して、プロパティ タグを取得して、値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティのタグを指定する必要があります。 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の次の値を指定します。
  
|||
|:-----|:-----|
|lpGuid。  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind。  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName。  <br/> |L"urn: スキーマ-マイクロソフト-com:office:outlook #serverfoldersizes」  <br/> |
   
Microsoft Outlook 2003 Service Pack (SP) 1年では、このプロパティがサポートされています。 Outlook のバージョンが Outlook 2003 SP 1 より前の場合、またはその値が**false**の場合は、ローカル ストアにフォルダーのサイズのみが表示されます。 このプロパティは、Outlook 2003 SP 1 を使用するストアに設定されている場合、Outlook は、サーバーとローカル ドライブに指定した各フォルダーのサイズを照会します。 
  
クエリを実行するサーバー上のフォルダーのサイズの Outlook フォルダーを開くと、ストアで[IMsgStore::OpenEntry](imsgstore-openentry.md)、 **MAPI_NO_CACHE**、このフラグを渡すと、 **PR_MESSAGE_SIZE_EXTENDED**を照会し、. ストア プロバイダーは、サーバー上でフォルダーのサイズを返す必要があります。
  
クエリを実行するローカル ドライブ上のフォルダーのサイズは、Outlook は、 **MAPI_NO_CACHE**フラグを設定しない] フォルダーを開きます。 それに基づいて、クエリの**PR_MESSAGE_SIZE_EXTENDED**です。ストア プロバイダーは、ローカル ドライブ上の指定したフォルダーのサイズを返す必要があります。
  
このプロパティを設定するストア プロバイダーをサーバーにストアの内容を同期は、Outlook の **[フォルダー サイズ**] ダイアログ ボックスでサーバーにフォルダーのサイズのデータを表示できます。 ユーザーは、現在のサーバー ストレージ使用状況とサーバーのクォータを比較し、ことができます。 
  
