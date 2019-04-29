---
title: メッセージストアプロバイダーでのテーブルのグループ化と制限
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428985"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>メッセージストアプロバイダーでのテーブルのグループ化と制限

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多くの場合、クライアントアプリケーションでは、フォルダーの内容の表示方法をユーザーが制御できます。 通常、ユーザーは1つまたは複数のメッセージプロパティの値に従ってグループ化されたメッセージを表示するか、または特定の条件に一致するメッセージを除外するかを選択できます。 これは、 [IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスを使用して行われます。 クライアントアプリケーションは、テーブルから返される行を、ユーザーが指定した条件に制限できます。 そのため、メッセージストアプロバイダーでは、次の**IMAPITable**メソッドを実装する必要があります。 
  
|IMAPITable * * メソッド * *|**説明**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |指定した条件に一致するテーブルの行を返します。  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |テーブル内の列のセット、または現在使用されている列のセットを返します。  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |指定された位置から開始して、1つまたは複数の行をテーブルから返します。  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |**FindRow**への後続の呼び出しが、制限に一致する行のみを返すようにテーブルに制限を適用します。  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |テーブルから行が取得されたときに返される列を指定します。  <br/> |
   
制限は、実装するのが複雑な場合があります。詳細については、「[制限につい](about-restrictions.md)て」を参照してください。 テーブルの実装の詳細については、「 [MAPI テーブル](mapi-tables.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

