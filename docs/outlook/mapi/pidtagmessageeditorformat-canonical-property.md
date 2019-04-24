---
title: PidTagMessageEditorFormat 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325635"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>PidTagMessageEditorFormat 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
エディターがメッセージの表示に使用する形式を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|識別子:  <br/> |0x5909  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>解説

**PR_MSG_EDITOR_FORMAT**に使用できる値は、次のいずれかです。 
  
|**値**|**説明**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |使用するエディターの形式が不明です。  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |エディターは、メッセージをプレーンテキスト形式で表示する必要があります。  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |エディターによって、メッセージが HTML 形式で表示されます。  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |エディターによって、メッセージがリッチテキスト形式で表示されます。  <br/> |
   
既定では、メールメッセージ (メッセージクラス**IPM.** または、IPM から派生したカスタムメッセージクラスを使用していることに注意**してください。注**) POP3/SMTP メールアカウントから送信されたメールは、トランスポートニュートラルカプセル化形式 (TNEF) で送信されます。 **PR_MSG_EDITOR_FORMAT**プロパティを使用すると、メッセージを送信するときに、TNEF ではなくプレーンテキストのみを適用できます。 **PR_MSG_EDITOR_FORMAT**が**EDITOR_FORMAT_PLAINTEXT**に設定されている場合、メッセージは TNEF なしのプレーンテキストとして送信されます。 **PR_MSG_EDITOR_FORMAT**が**EDITOR_FORMAT_RTF**に設定されている場合、TNEF エンコードは暗黙的に有効になり、メッセージは Outlook クライアントで指定された既定のインターネット形式を使用して送信されます。
  
メッセージを送信するときに TNEF の使用を強制するには、他に2つの方法があります。
  
- メッセージで**dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) 名前付きプロパティを True に設定することは、メッセージを MAPI から MIME/SMTP に変換するときに、TNEF を含める必要があることを示しています。 **dispidUseTNEF**は、メッセージが POP3/SMTP メールアカウントから送信された場合にのみ適用されることに注意してください。また、メッセージが他のプロバイダー (Microsoft Exchange Server など) によって送信された場合には適用されません。 **dispidUseTNEF**は、 **PR_MSG_EDITOR_FORMAT**の設定より優先されます。
    
- [iconvertersession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を呼び出して**CCSF_USE_TNEF**フラグを使用すると、送信 MAPI メッセージを MIME ストリームに変換できます。また、TNEF を強制することもできます。 これは、 **dispidUseTNEF**が設定されていない場合でも適用されます。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本データ構造を定義します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
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

