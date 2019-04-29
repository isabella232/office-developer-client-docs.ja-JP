---
title: テーブルの行からデータを取得する
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
# <a name="retrieving-data-from-table-rows"></a>テーブルの行からデータを取得する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルから行を取得するには、次の処理が必要です。
  
- すべての列のプロパティ値を取得します。
    
- 現在の位置を変更します。
    
ほとんどのテーブルで必要な列の1つはエントリ識別子 ( **** [PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティで、これを使用して行を表すオブジェクトを開くことができます。 このエントリ識別子は、通常、短い用語のエントリ識別子です。これは、テーブルの有効期間を超えて保持されないものです。 ただし、テーブルを実装するサービスプロバイダーが1つの種類のエントリ識別子のみをサポートする場合は、長期の識別子になることがあります。
  
クライアントとサービスプロバイダーは、次のいずれかの呼び出しを行って行を取得できます。
  
|||
|:-----|:-----|
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |前方または後方のどちらかの方向に、現在の行から始まる指定された数の行を取得します。  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |テーブル内のすべての行を取得します。  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |インデックス列の値に従って、テーブル内の行を取得します。 **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) は、通常、テーブルのインデックス列です。  <br/> |
   
オプションのプロパティがテーブルの列の1つとして含まれている場合、一部の行には列に有効な値が含まれている場合がありますが、それ以外の場合もあります。 列に有効な値が存在するかどうかは、その行の情報を提供するオブジェクトがプロパティを設定するかどうかによって決まります。 オブジェクトの実装によっては、存在しないプロパティをテーブルで**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) または任意の値として表すことができます。 テーブルのユーザーは、存在しないプロパティと、存在しない値および有効な値を持つプロパティを慎重に区別する必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

