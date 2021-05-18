---
title: テーブル行からのデータの取得
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2f389d26ec80b9af3ed28c5eb85b589c9cbb26c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405255"
---
# <a name="retrieving-data-from-table-rows"></a>テーブル行からのデータの取得

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルから行を取得するには、次の処理が必要です。
  
- すべての列のプロパティ値を取得します。
    
- 現在の位置を変更します。
    
ほとんどのテーブルで必要な列の **1 つは、PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティというエントリ識別子で、行を表すオブジェクトを開くのに使用できます。 このエントリ識別子は、通常、短期的なエントリ識別子で、テーブルの有効期間を過ぎた後も保持されません。 ただし、テーブルを実装するサービス プロバイダーが 1 種類のエントリ識別子のみをサポートしている場合は、長期的な識別子を指定できます。
  
クライアントとサービス プロバイダーは、次のいずれかの呼び出しを行って行を取得できます。
  
|||
|:-----|:-----|
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |現在の行から順方向または逆方向の行で始まる、指定した数の行を取得します。  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |テーブル内のすべての行を取得します。  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |インデックス列の値に従ってテーブル内の行を取得します。 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) は、通常、テーブルのインデックス列です。  <br/> |
   
省略可能なプロパティを表の列の 1 つとして含める場合、一部の行には列に対して有効な値を持つ場合があります。一部の行には有効な値が含まれていない場合があります。 列に有効な値が存在するかどうかは、行の情報を提供するオブジェクトがプロパティを設定するかどうかによって異なります。 オブジェクトの実装に応じて、存在しないプロパティを **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) または任意の値として表します。 テーブルのユーザーは、存在しないプロパティと、存在し、有効な値を持つ無意味な値とプロパティを区別するために注意する必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

