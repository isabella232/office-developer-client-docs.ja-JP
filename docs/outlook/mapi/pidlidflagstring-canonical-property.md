---
title: PidLidFlagString 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357786"
---
# <a name="pidlidflagstring-canonical-property"></a>PidLidFlagString 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フラグに関連付けられた定義済みのテキスト文字列のセットのいずれかを識別するインデックスを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidFlagStringEnum  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085C0  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティが設定されている場合、クライアントは以下の表で対応する文字列値を使用する必要があります (たとえば、現在のユーザーの言語に変換される文字列を置き換える場合 **)、dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) と **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) で設定された値を無視する必要があります。 
  
連絡先オブジェクトに対してユーザーに提案される既定値は次のとおりです。
  
|**値**|**英語の文字列**|
|:-----|:-----|
|0x00000000または存在しない  <br/> | **dispidFlagRequest の表示に関連するガイダンスに従います**。  <br/> |
|0x0000006E  <br/> |"フォローアップ"  <br/> |
|0x0000006F  <br/> |"Call"  <br/> |
|0x00000070  <br/> |"会議の手配"  <br/> |
|0x00000071  <br/> |"メールの送信"  <br/> |
|0x00000072  <br/> |"Send Letter"  <br/> |
   
他のすべてのメッセージ オブジェクトに対してユーザーに提案される既定値は次のとおりです。
  
|**値**|**英語の文字列**|
|:-----|:-----|
|0x00000000または存在しない  <br/> | **dispidFlagRequest の表示に関連するガイダンスに従います**。  <br/> |
|0x00000001  <br/> |"Call"  <br/> |
|0x00000002  <br/> |"転送しない"  <br/> |
|0x00000003  <br/> |"フォローアップ"  <br/> |
|0x00000004  <br/> |"For Your Information"  <br/> |
|0x00000005  <br/> |"転送する"  <br/> |
|0x00000006  <br/> |"応答不要"  <br/> |
|0x00000007  <br/> |"Read"  <br/> |
|0x00000008  <br/> |"返信"  <br/> |
|0x00000009  <br/> |"全員に返信"  <br/> |
|0x0000000A  <br/> |"Review"  <br/> |
   
上記で指定した文字列はすべて、必要に応じてユーザーの言語に変換できます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

