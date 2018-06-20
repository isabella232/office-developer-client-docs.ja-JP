---
title: PidTagTnefCorrelationKey の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5a0216616d9a35ef5ad4509bc377044c1d217d79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803633"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>PidTagTnefCorrelationKey の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ トランスポート ニュートラル カプセル化形式 (TNEF) の添付ファイルを対応する値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|識別子:  <br/> |0x007f まで  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>備考

TNEF の添付ファイルのサブ オブジェクトがこのプロパティを公開することをお勧めします。 このプロパティは、接続しているメッセージを受信の TNEF ファイルが属しているかどうかを決定します。 トランスポート プロバイダーおよびゲートウェイによって主に使用されます。
  
送信メッセージでは、トランスポート プロバイダーは、そのメッセージに一意のバイナリ値を計算またはメッセージ id など、一意性の必要条件を満たす既存の値を使用します。 トランスポート プロバイダーは、このプロパティにこの値を格納し、それをカプセル化する[ITnef::AddProps](itnef-addprops.md)メソッドを呼び出してください。 同じ値は、メッセージ ヘッダーなど、プロバイダーによって定義された場所にトランスポート エンベロープにも保存されます。 
  
受信メッセージでは、トランスポート プロバイダーは、必要があります TNEF 添付ファイルをカプセル化解除する[ITnef::ExtractProps](itnef-extractprops.md)メソッドを呼び出すし、トランスポート エンベロープに格納されている値にこのプロパティを比較します。 値が一致した場合は、TNEF を正常に処理する必要がありますは、TNEF 添付ファイルから抽出されたすべてのプロパティを使用する必要があります。 値が一致しない場合は、TNEF の添付ファイルからのすべてのプロパティは無視されます。 このプロパティが設定されていない場合に属しているこのメッセージの TNEF ファイルを考慮する必要があり、そこから抽出された他のプロパティを使用する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> 順序と、クライアントとサーバー間のデータ転送のフローを処理します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
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

