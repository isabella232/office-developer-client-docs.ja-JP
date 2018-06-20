---
title: PidLidFlagString の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 53fe309fb15807ad698fef5a06781e5c3e0bae0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801984"
---
# <a name="pidlidflagstring-canonical-property"></a>PidLidFlagString の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
フラグに関連付けられている定義済みのテキスト文字列のセットのいずれかを識別するインデックスが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidFlagStringEnum  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085C0  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

クライアントが (たとえば、現在のユーザーの言語に翻訳された文字列を置換する)、以下の表に対応する文字列値を使用する必要があり、 **dispidFlagRequest** ([で設定された値を無視する必要がありますこのプロパティが設定されている場合PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) と**dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md))。 
  
連絡先オブジェクトをユーザーに推奨される既定値は次のとおりです。
  
|**値**|**英語の文字列**|
|:-----|:-----|
|0x00000000 されていないか  <br/> | **DispidFlagRequest**の表示に関連する指示に従います。  <br/> |
|0x0000006E  <br/> |「フォロー アップ」  <br/> |
|0x0000006F  <br/> |「呼び出し」  <br/> |
|0x00000070  <br/> |「会議を開催」  <br/> |
|0x00000071  <br/> |[電子メールを送信する]  <br/> |
|0x00000072  <br/> |"の文字を送信する]  <br/> |
   
他のすべてのメッセージ オブジェクトのユーザーに推奨される既定値は次のとおりです。
  
|**値**|**英語の文字列**|
|:-----|:-----|
|0x00000000 されていないか  <br/> | **DispidFlagRequest**の表示に関連する指示に従います。  <br/> |
|0x00000001  <br/> |「呼び出し」  <br/> |
|0x00000002  <br/> |「転送不可」  <br/> |
|0x00000003  <br/> |「フォロー アップ」  <br/> |
|0x00000004  <br/> |"については、「  <br/> |
|0x00000005  <br/> |「転送」  <br/> |
|0x00000006  <br/> |「返信不要」  <br/> |
|0x00000007  <br/> |「読み取り」  <br/> |
|0x00000008  <br/> |[返信]  <br/> |
|0x00000009  <br/> |"全員へ返信]  <br/> |
|0x0000000A  <br/> |「レビュー」  <br/> |
   
上で指定したすべての文字列は、適切な場合、ユーザーの言語に翻訳できます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

