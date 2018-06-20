---
title: PidTagRtfSyncBodyCount の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 09274c21df3a93abc19aa8158da976e2d16f3e7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803407"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a>PidTagRtfSyncBodyCount の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
重要なメッセージのテキストの文字数が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_RTF_SYNC_BODY_COUNT  <br/> |
|識別子:  <br/> |0x1007  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI メッセージ  <br/> |
   
## <a name="remarks"></a>備考

[](rtfsync.md)関数は、メッセージに重要と見なされるものだけを使用してテキスト内の文字数を計算します。 などのいくつかの空白および他の無視可能な文字はカウントから省略されます。 
  
このプロパティは、リッチ テキスト形式 (RTF) 補助プロパティです。 これらのプロパティ**へ**の関数で使用され、クライアント アプリケーションで直接使用するものではありません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

