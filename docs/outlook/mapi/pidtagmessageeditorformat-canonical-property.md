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
ms.openlocfilehash: a6a3eb88377777a3d27687179bfdcb82057be3a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802988"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>PidTagMessageEditorFormat 標準プロパティ

  
  
**適用対象**: Outlook 
  
エディターを使用してメッセージを表示する形式を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|識別子:  <br/> |0x5909  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>注釈

**PR_MSG_EDITOR_FORMAT**の有効な値には、次のいずれかを指定できます。 
  
|**値**|**説明**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |使用するエディターの形式が不明です。  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |エディターは、テキスト形式でメッセージを表示する必要があります。  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |エディターは、HTML 形式でメッセージを表示する必要があります。  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |エディターでは、リッチ テキスト形式でメッセージを表示する必要があります。  <br/> |
   
既定では、メールのメッセージ (メッセージ クラス IPM の**です。注**またはカスタム メッセージ クラスが IPM の**から派生します。注意してください**) 送信される POP3 または SMTP メールのアカウントはトランスポート ニュートラル カプセル化形式 (TNEF) で送信されます。 メッセージを送信するときに、プレーン テキストと、TNEF ではないだけを適用するのには、 **PR_MSG_EDITOR_FORMAT**プロパティを使用できます。 **PR_MSG_EDITOR_FORMAT**は、 **EDITOR_FORMAT_PLAINTEXT**に設定されている場合は、メッセージが TNEF なしのテキストとして送信されます。 **PR_MSG_EDITOR_FORMAT**は、 **EDITOR_FORMAT_RTF**に設定されている場合は、TNEF エンコードは暗黙的に有効になっていると Outlook クライアントで指定されている既定のインターネット メール形式を使用してメッセージを送信します。
  
メッセージを送信するときは、TNEF の使用を強制する他の 2 つの方法があります。
  
- **DispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) という名前のプロパティをメッセージに True を設定するには、MAPI から MIME と SMTP メッセージに変換するときは、TNEF を付属する必要があることを示します。 その**dispidUseTNEF**は、メッセージは、POP3 または SMTP のメール アカウントから送信され、Microsoft Exchange Server など、他のプロバイダーによって、メッセージが送信されるときは適用されませんがある場合にのみ適用されますに注意してください。 **dispidUseTNEF**は、 **PR_MSG_EDITOR_FORMAT**の設定を上書きします。
    
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を呼び出すときに**CCSF_USE_TNEF**フラグを使用して送信、MAPI メッセージを MIME ストリームに変換すると、TNEF にも適用できます。 これは、 **dispidUseTNEF**が設定されていない場合でも適用されます。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本的なデータ構造を定義します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
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

