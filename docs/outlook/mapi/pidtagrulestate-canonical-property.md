---
title: PidTagRuleState 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c28c4af9117ca0aee1b19ecef812c2636860c45c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599495"
---
# <a name="pidtagrulestate-canonical-property"></a>PidTagRuleState 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ルールの状態を指定するフラグのビットマスクの組み合わせとして解釈される値。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RULE_STATE  <br/> |
|識別子:  <br/> |0x6677  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>注釈

次の表は、このプロパティの可能な値を定義します。
  
EN (ST_ENABLED、ビットマスク0x00000001)
  
> ルールは実行に対して有効です。 このフラグが設定されていない場合、ルールの評価時にサーバーは、このルールをスキップする必要があります。
    
ER (ST_ERROR、ビットマスク0x00000002)
  
> サーバーでルールの処理中にエラーが発生しました。
    
OF (ST_ONLY_WHEN_OOF、ビットマスク0x00000004)
  
> このルールは、ユーザーがメールボックスの [出力Office (OOF) 状態を設定した場合にのみ実行されます。 このフラグは、パブリック フォルダー ルールで設定することはできません。
    
HI (ST_KEEP_OOF_HIST、ビットマスク0x00000008)
  
> このフラグは、パブリック フォルダー ルールで設定することはできません。
    
EL (ST_EXIT_LEVEL、ビットマスク0x00000010)
  
> ルールの評価は、このルールの実行後に終了します。ただし、Out of Officeです。
    
SCL (ST_SKIP_IF_SCL_IS_SAFE、ビットマスク0x00000020)
  
> このルールの評価はスキップされる場合があります。
    
PE (ST_RULE_PARSE_ERROR、ビットマスク0x00000040)
  
> サーバーで、クライアントによって提供されたルール データの解析中にエラーが発生しました。
    
X
  
> このプロトコルでは使用されません。 このビットは、クライアントによって変更する必要があります。
    
次に示すフラグとST_ONLY_WHEN_OOFフラグST_EXIT_LEVEL注意してください。 
  
メールボックスで "out of Office" 状態が設定され、ルール条件が TRUE に評価された場合、 
  
そして：
  
- ルールには、ST_EXIT_LEVELフラグが設定され、ST_ONLY_WHEN_OOF設定されていない。 次に、サーバーは、このフラグが設定されていない後続のルールを評価ST_ONLY_WHEN_OOFし、フラグが設定されている後続のルールST_ONLY_WHEN_OOFする必要があります。
    
OR:
  
- ルールには、ST_EXIT_LEVELフラグST_ONLY_WHEN_OOFがあります。 その後、サーバーは後続のルールを評価しなけらね。
    
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

