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
ms.openlocfilehash: 9d1adb6dd1fc151c9a599ea44391c2ca5b2fe2aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580566"
---
# <a name="pidtagrulestate-canonical-property"></a>PidTagRuleState 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ルールの状態を指定するフラグのビットマスクの組み合わせとして解釈される値です。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RULE_STATE  <br/> |
|識別子:  <br/> |0x6677  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>注釈

次の表は、このプロパティの値を定義します。
  
EN (ST_ENABLED、0x00000001 のビットマスク)
  
> ルールは実行するために有効です。 このフラグが設定されていない場合、サーバーでは、ルールを評価するときにこのルールにスキップします。
    
ER (ST_ERROR、ビットマスク 0x00000002)
  
> サーバーは、ルールを処理中にエラーが発生しました。
    
(ST_ONLY_WHEN_OOF、ビットマスク 0x00000004) の
  
> ルールは、ユーザー メールボックスの不在時の Office (OOF) の状態を設定する場合にのみ実行されます。 パブリック フォルダーのルールで、このフラグを設定しないでください。
    
HI (ST_KEEP_OOF_HIST、ビットマスク 0x00000008)
  
> パブリック フォルダーのルールで、このフラグを設定しないでください。
    
EL (ST_EXIT_LEVEL、ビットマスク 0x00000010)
  
> ルールの評価は、Office のうち、ルールの評価の場合を除き、この規則を実行した後終了します。
    
SCL (ST_SKIP_IF_SCL_IS_SAFE、ビットマスク 0x00000020)
  
> このルールの評価をスキップすることがあります。
    
PE (ST_RULE_PARSE_ERROR、ビットマスク 0x00000040)
  
> サーバー、クライアントによって提供される規則のデータを解析中にエラーが発生しました。
    
X
  
> このプロトコルが使用されていません。 クライアントが、このビットを変更しないでください。
    
フラグの ST_ONLY_WHEN_OOF と ST_EXIT_LEVEL 間の相互作用に注意してください。 
  
メールボックスの [不在時の Office"状態に設定し、ルール条件の評価が true の場合、 
  
そして：
  
- ルールがあり、ST_EXIT_LEVEL フラグを設定、ST_ONLY_WHEN_OOF フラグが設定されていることはありません。 サーバーが ST_ONLY_WHEN_OOF する必要はありません後のルールを評価する必要があります、セットのフラグを設定し、ST_ONLY_WHEN_OOF フラグが設定された後のルールを評価する必要があります。
    
OR:
  
- ルールが、ST_EXIT_LEVEL と ST_ONLY_WHEN_OOF の両方のフラグを設定します。 サーバーする必要があります、その後のルールを評価しません。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> サーバー上の受信電子メール メッセージを操作します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

