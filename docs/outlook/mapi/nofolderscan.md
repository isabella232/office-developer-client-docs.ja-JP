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
  
Microsoft Office Outlook がストアの連絡先フォルダーをスキャンする必要があるかどうかを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|公開:  <br/> |[IMsgStore: imapiprop](imsgstoreimapiprop.md)オブジェクト  <br/> |
|作成者:  <br/> |ストアプロバイダー  <br/> |
|アクセス先:  <br/> |Outlook およびその他のクライアント  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|アクセスの種類:  <br/> |ストアプロバイダーに応じて読み取り専用または読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

ストアの機能を提供するには、ストアプロバイダーが[imapiprop: IUnknown](imapipropiunknown.md)を実装し、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)呼び出しに渡されるこれらのプロパティに対して有効なプロパティタグを返す必要があります。 これらのプロパティのいずれかのプロパティタグが[imapiprop:: GetProps](imapiprop-getprops.md)に渡されると、ストアプロバイダーは、適切なプロパティ値を返す必要があります。 ストアプロバイダーは、 [hrgetoneprop](hrgetoneprop.md)および[hrgetoneprop](hrsetoneprop.md)を呼び出して、これらのプロパティを取得または設定できます。 
  
このプロパティの値を取得するには、クライアントはまず[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を使用してプロパティタグを取得し、次に[imapiprop:: GetProps](imapiprop-getprops.md)でこのプロパティタグを指定して値を取得する必要があります。 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lpppropnames_でポイントされている[mapinameid](mapinameid.md)構造に次の値を指定します。
  
|||
|:-----|:-----|
|lpguid:  <br/> |PSETID_Common  <br/> |
|ulkind:  <br/> |MNID_STRING  <br/> |
|種類が lpwstrname:  <br/> |L "nofolderscan"  <br/> |
   
このプロパティは、ストアプロバイダーが、パフォーマンスの低下を回避するためにストア内の連絡先フォルダーをスキャンしないように指定する方法を提供します。 これは、Outlook がスキャンを開始する前に、このプロパティのプレゼンスと値をチェックする差し込み印刷操作で使用されます。
  
既定では、このプロパティはストアに公開されていないため、Outlook はストアの連絡先フォルダーをスキャンできます。 プロパティが公開されている場合は、次の値を指定できます。
  
- ゼロ (0): Outlook はスキャンを実行できます。
    
- 0以外の値: Outlook は、ストア上の連絡先フォルダーをスキャンしません。
    

