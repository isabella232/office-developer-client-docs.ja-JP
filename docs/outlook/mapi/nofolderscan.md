---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436812"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストアの連絡先Microsoft Office Outlookスキャンするかどうかを指定します。
  
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
|Kind.lpwstrName:  <br/> |L"NoFolderScan"  <br/> |
   
このプロパティを使用すると、ストア プロバイダーは、パフォーマンスの低下を避けるために、Outlook連絡先フォルダーをスキャンしないように指定できます。 これは、スキャンを開始する前に、Outlookプロパティの存在と値をチェックする差し込み印刷操作で使用されます。
  
既定では、このプロパティはストアで公開されません。つまり、Outlook連絡先フォルダーをスキャンできます。 プロパティが公開されている場合は、次の値を使用できます。
  
- ゼロ (0): Outlookを実行できます。
    
- ゼロ以外の値: ストアOutlook連絡先フォルダーをスキャンしない必要があります。
    

