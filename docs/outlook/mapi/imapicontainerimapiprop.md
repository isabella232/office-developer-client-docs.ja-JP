---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5a76b5cb08e098235dda03df81becf9b15c6ee69
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610658"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳、配布リスト、フォルダーなどのコンテナー オブジェクトに対する高レベルの操作を管理します。 [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md)インターフェイスは **IMAPIContainer から派生しています**。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |フォルダー、アドレス帳コンテナー、配布リスト オブジェクト  <br/> |
|実装元:  <br/> |メッセージ ストア、アドレス帳、およびリモート トランスポート プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIContainer  <br/> |
|ポインターの種類:  <br/> |LPMAPICONTAINER  <br/> |
|トランザクション モデル:  <br/> |抽象クラス(実装されていない)  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |コンテナーのコンテンツ テーブルへのポインターを返します。  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |コンテナーの階層テーブルへのポインターを返します。  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |コンテナー内のオブジェクトを開き、さらにアクセスするインターフェイス ポインターを返します。  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |コンテナーの検索条件を設定します。  <br/> |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |コンテナーの検索条件を取得します。  <br/> |
   
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

