---
title: グループ化し、メッセージ ストア プロバイダーのテーブルを制限します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 33c76cdd0e7850f82949349ac2e5bb0dd4e056ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800172"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>グループ化し、メッセージ ストア プロバイダーのテーブルを制限します。

  
  
**適用されます**: Outlook 
  
クライアント アプリケーション頻繁にできるように、フォルダーの内容を表示する方法を制御します。 通常、ユーザーはメッセージを 1 つまたは複数のメッセージのプロパティの値に基づいてグループ化することができますか、特定の条件に一致するメッセージを除外することができます。 使用して、これは、 [IMAPITable: IUnknown](imapitableiunknown.md)インタ フェースです。 クライアント アプリケーションは、ユーザーが指定されている基準に、テーブルから返される行を制限できます。 したがって、メッセージは、次**IMAPITable**メソッドを実装するプロバイダーのニーズを格納します。 
  
|* * IMAPITable メソッド * *|**説明**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |テーブルの指定した条件に一致する行を返します。  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |テーブルまたは現在使用されている列のセット内の列のセットを返します。  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |指定した位置から、テーブルから 1 つまたは複数の行を返します。  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |**FindRow**の以降の呼び出しが制限に一致する行だけを返すには、制限テーブルに適用されます。  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |行はテーブルから取得するときに返される列を指定します。  <br/> |
   
制限を実装するのには複雑になること詳細については、[制限の詳細](about-restrictions.md)を参照してください。 テーブルを実装する方法の詳細については、 [MAPI テーブル](mapi-tables.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)
