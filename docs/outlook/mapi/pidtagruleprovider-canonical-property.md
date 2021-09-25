---
title: PidTagRuleProvider 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 32a0e900c959b17dd7b1e61bdaa9c80a6f5d4966
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591480"
---
# <a name="pidtagruleprovider-canonical-property"></a>PidTagRuleProvider 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ルールを設定するアプリケーションの名前を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RULE_PROVIDER、PR_RULE_PROVIDER_A、PR_RULE_PROVIDER_W  <br/> |
|識別子:  <br/> |0x6681  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>注釈

遅延アクションでは、ルール アクションを解釈して実行する必要があるコードを識別するために、これらのプロパティが必要です。
  
メールボックスとフォルダーに格納されているルールは、ルール プロバイダー文字列によってそれらを所有するアプリケーションに関連付けられる。 ルール プロバイダーは、ルール テーブル内のルールを設定および処理します。 また、そのようなルールが設定されている場合に遅延アクションを処理する手段も提供します。 遅延アクションは、情報ストアによって暗黙的に作成されます。 別のストアへの移動またはコピー操作の場合、プロバイダーが遅延アクション ルールを設定する場合は、ルールが発生し、遅延アクションが作成された場合にアクションを実行するためのハンドラーを提供する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> サーバー上の受信メール メッセージを操作します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

