---
title: IMAPIContainer IMAPIProp
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
ms.openlocfilehash: 38094895fed03884b138b02d4aa1ed87bcc6ea9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575701"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
アドレス帳、配布リスト、フォルダーなどのコンテナー オブジェクトの高度な処理を管理します。 [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)、[これにより: IMAPIContainer](iabcontainerimapicontainer.md)、および[IDistList: IMAPIContainer](idistlistimapicontainer.md)インタ フェースは、 **IMAPIContainer**から派生します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |フォルダー、アドレス帳コンテナー、および配布リスト内のオブジェクト  <br/> |
|によって実装されます。  <br/> |メッセージ ・ ストア、アドレス帳、およびリモート トランスポート プロバイダー  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIContainer  <br/> |
|ポインターの型。  <br/> |LPMAPICONTAINER  <br/> |
|トランザクション モデル:  <br/> |抽象クラスで実装されることはありません。  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |コンテナーの内容のテーブルへのポインターを返します。  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |コンテナーの階層構造のテーブルへのポインターを返します。  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |コンテナーで、さらにアクセスするためのインターフェイス ポインターを返すには、オブジェクトを開きます。  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |コンテナーの検索基準を確立します。  <br/> |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |コンテナーの検索条件を取得します。  <br/> |
   
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_CONTAINER_FLAGS**([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

