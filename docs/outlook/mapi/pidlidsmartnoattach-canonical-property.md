---
title: PidLidSmartNoAttach の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSmartNoAttach
api_type:
- COM
ms.assetid: 60299c1b-1b46-4c3a-8fb9-a2b4d3383aac
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 43e10652a7dccdf0da6592df0f9fc2daf5ea9bee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802166"
---
# <a name="pidlidsmartnoattach-canonical-property"></a>PidLidSmartNoAttach の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージの添付ファイルと見なされますかどうかを非表示にします。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidSmartNoAttach  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008514  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>備考

メッセージの添付ファイルと見なされる場合は、このプロパティは TRUE を非表示にします。
  
これは、メッセージ オブジェクトのエンド ・ ユーザーに表示されている添付ファイルがないかどうかを示します。 このプロパティが設定ではない可能性があります。既定値は FALSE と見なされます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

