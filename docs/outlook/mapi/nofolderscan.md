---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3416bc50e4628df2be09f9fe1a22d19530bcdff8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578053"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
Microsoft Office Outlook がストアの連絡先フォルダーをスキャンするかどうかを指定します。
  
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
|Kind.lpwstrName。  <br/> |L"NoFolderScan"  <br/> |
   
このプロパティは、Outlook を指定するのには、ストア プロバイダーのパフォーマンスの低下を防ぐためにストア内の連絡先フォルダーをスキャンする方法を提供します。 スキャンを開始する前に存在し、このプロパティの値を調べ、差し込み印刷操作で使用されます。
  
既定では、このプロパティは、ストアは、Outlook は、ストアの連絡先フォルダーをスキャンできることを意味では公開されません。 プロパティが公開されている場合、値は次のことです。
  
- ゼロ (0): Outlook は、スキャンを実行できます。
    
- ゼロ以外の値: Outlook では、ストアの連絡先フォルダーはスキャンする必要があります。
    

