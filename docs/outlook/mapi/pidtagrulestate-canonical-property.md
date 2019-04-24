---
title: PidTagRuleState 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338613"
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
   
## <a name="remarks"></a>解説

次の表では、このプロパティに指定できる値を定義します。
  
EN (ST_ENABLED、ビットマスク 0x00000001)
  
> ルールは実行に対して有効になっています。 このフラグが設定されていない場合、ルールを評価するときに、サーバーはこのルールをスキップする必要があります。
    
ER (ST_ERROR、ビットマスク 0x00000002)
  
> サーバーでルールの処理中にエラーが発生しました。
    
OF (ST_ONLY_WHEN_OOF, ビットマスク 0x00000004)
  
> このルールは、ユーザーがメールボックスの不在 (OOF) 状態を設定した場合にのみ実行されます。 このフラグは、パブリックフォルダーのルールに設定することはできません。
    
HI (ST_KEEP_OOF_HIST, ビットマスク 0x00000008)
  
> このフラグは、パブリックフォルダーのルールに設定することはできません。
    
EL (ST_EXIT_LEVEL、ビットマスク 0x00000010)
  
> ルールの評価は、不在時ルールの評価を除き、このルールを実行した後に終了します。
    
SCL (ST_SKIP_IF_SCL_IS_SAFE、ビットマスク 0x00000020)
  
> このルールの評価はスキップされる可能性があります。
    
PE (ST_RULE_PARSE_ERROR、ビットマスク 0x00000040)
  
> クライアントによって提供されたルールデータの解析中にサーバーでエラーが発生しました。
    
X
  
> このプロトコルでは使用されません。 このビットは、クライアントが変更することはできません。
    
ST_ONLY_WHEN_OOF フラグと ST_EXIT_LEVEL フラグの間の相互作用に関する注意事項: 
  
"不在" 状態がメールボックスに設定されており、ルールの条件が TRUE と評価される場合は、 
  
そして：
  
- ルールに ST_EXIT_LEVEL フラグが設定されていて、ST_ONLY_WHEN_OOF フラグが設定されていません。 次に、ST_ONLY_WHEN_OOF フラグが設定されていない後続のルールをサーバーが評価しないようにして、ST_ONLY_WHEN_OOF フラグが設定されている後続のルールを評価する必要があります。
    
や
  
- ルールには、ST_EXIT_LEVEL と ST_ONLY_WHEN_OOF の両方のフラグが設定されています。 その後、サーバーは後続のルールを評価しないようにする必要があります。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> サーバー上の受信電子メールメッセージを操作します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

