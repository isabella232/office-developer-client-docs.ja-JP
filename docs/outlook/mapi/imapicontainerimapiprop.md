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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e24f5ebd73a4652876282099f1460762c150b94d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800455"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer: IMAPIProp

  
  
**適用されます**: Outlook 
  
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
   
|**必要なプロパティ**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_CONTAINER_FLAGS**([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

