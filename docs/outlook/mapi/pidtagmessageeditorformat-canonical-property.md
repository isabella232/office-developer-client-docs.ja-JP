---
title: PidTagMessageEditorFormat 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dd107de00ebc7ab55b6d255c4bc993d9c3210086
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560887"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>PidTagMessageEditorFormat 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの表示に使用するエディターの形式を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|識別子:  <br/> |0x5909  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>注釈

指定できる値は **PR_MSG_EDITOR_FORMAT** のいずれかを指定できます。 
  
|**値**|**説明**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |エディターで使用する形式が不明です。  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |エディターはメッセージをプレーン テキスト形式で表示する必要があります。  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |エディターはメッセージを HTML 形式で表示する必要があります。  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |エディターはリッチ テキスト形式でメッセージを表示する必要があります。  <br/> |
   
既定では、メール メッセージ (メッセージ クラス **IPM を含む)。メモ** または IPM から派生したカスタム メッセージ クラス **を使用します。注**) は、POP3/SMTP メール アカウントから送信され、トランスポート ニュートラル カプセル化形式 (TNEF) で送信されます。 PR_MSG_EDITOR_FORMATプロパティ **を** 使用すると、メッセージの送信時に TNEF ではなくプレーン テキストのみを適用できます。 この **PR_MSG_EDITOR_FORMAT** に **設定されている場合** EDITOR_FORMAT_PLAINTEXT、メッセージは TNEF なしでプレーン テキストとして送信されます。 PR_MSG_EDITOR_FORMAT **が** **EDITOR_FORMAT_RTF** に設定されている場合、TNEF エンコードは暗黙的に有効にされ、メッセージはクライアントで指定された既定のインターネット形式を使用してOutlookされます。
  
メッセージの送信時に TNEF の使用を強制するには、他に 2 つの方法があります。
  
- メッセージの **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) 名前付きプロパティを True に設定すると、MAPI から MIME/SMTP にメッセージを変換するときに TNEF を含める必要があります。 **dispidUseTNEF** は、メッセージが POP3/SMTP メール アカウントから送信された場合にのみ適用され、メッセージが Microsoft Exchange Server などの他のプロバイダーによって送信された場合は適用されません。 **dispidUseTNEF は**、 の設定を **オーバーライドPR_MSG_EDITOR_FORMAT。**
    
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を呼び出す際に CCSF_USE_TNEF フラグを使用して発信 MAPI メッセージを MIME ストリームに変換すると、TNEF も強制できます。  これは **、dispidUseTNEF** が設定されていない場合でも適用されます。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本的なデータ構造を定義します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
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

