---
title: メッセージ ストア プロバイダーのテーブルのグループ化と制限
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
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>メッセージ ストア プロバイダーのテーブルのグループ化と制限

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションでは、フォルダーの内容の表示方法をユーザーが制御できる場合が多い。 通常、ユーザーは、1 つ以上のメッセージ プロパティの値に従ってメッセージをグループ化するか、特定の条件に一致するメッセージを除外することもできます。 これは [、IMAPITable : IUnknown インターフェイスを使用して行](imapitableiunknown.md) います。 クライアント アプリケーションは、テーブルから返される行を、ユーザーが指定した条件に制限できます。 したがって、メッセージ ストア プロバイダーは、次の **IMAPITable メソッドを実装する** 必要があります。 
  
|IMAPITable** メソッド**|**説明**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |指定した条件に一致するテーブル行を返します。  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |テーブル内の列のセットまたは現在使用されている列のセットを返します。  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |指定した位置から始まる、テーブルから 1 つ以上の行を返します。  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |テーブルに制限を適用して **、FindRow** への後続の呼び出しが制限に一致する行のみを返します。  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |テーブルから行を取得するときに返す列を指定します。  <br/> |
   
制限は、実装が複雑になる場合があります。詳細については、「制限について [」を参照してください](about-restrictions.md)。 テーブルの実装の詳細については、「MAPI テーブル」 [を参照してください](mapi-tables.md)。
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

