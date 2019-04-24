---
title: IMAPIContainer imapiprop
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8be3b1857d539f81e42d2ac3e5813afa73513a16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286721"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳、配布リスト、フォルダーなどのコンテナーオブジェクトの高レベルの操作を管理します。 [imapifolder: IMAPIContainer](imapifolderimapicontainer.md)、 [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)、および[idistlist: IMAPIContainer](idistlistimapicontainer.md)インターフェイスは、 **IMAPIContainer**から派生します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |フォルダー、アドレス帳コンテナー、および配布リストオブジェクト  <br/> |
|実装元:  <br/> |メッセージストア、アドレス帳、リモートトランスポートプロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIContainer  <br/> |
|ポインターの種類:  <br/> |LPMAPICONTAINER  <br/> |
|トランザクションモデル:  <br/> |抽象クラス、実装されていません  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[getcontentstable](imapicontainer-getcontentstable.md) <br/> |コンテナーの contents テーブルへのポインターを返します。  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |コンテナーの階層テーブルへのポインターを返します。  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |コンテナー内のオブジェクトを開き、さらにアクセスするためのインターフェイスポインターを返します。  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |コンテナーの検索条件を確立します。  <br/> |
|[getsearchcriteria](imapicontainer-getsearchcriteria.md) <br/> |コンテナーの検索条件を取得します。  <br/> |
   
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_CONTAINER_FLAGS**([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

