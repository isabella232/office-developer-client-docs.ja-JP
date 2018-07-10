---
title: PidTagJunkThreshold の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0f8484e195b1cda8e1d633133cdff89c571d8ecd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802915"
---
# <a name="pidtagjunkthreshold-canonical-property"></a>PidTagJunkThreshold の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
どの程度積極的に示す [迷惑メール] フォルダーに受信メールを送信する必要があります。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_JUNK_THRESHOLD  <br/> |
|識別子:  <br/> |0x6101  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |スパム  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、高と低に対応/の設定にフィルターを適用します。 "0 xffffffff"の値は、ブロック リストを適用する必要がありますが、スパム フィルターが適用されないことを示します。 「0x80000000」値は、すべてのメールはを除き、これらのメッセージの差出人セーフ リストに送信者からの迷惑メールや、信頼された受信者リストの受信者に送信されることを示します。 この値は次のとおりです。
  
|**値**|**説明**|
|:-----|:-----|
|0 xffffffff  <br/> |なしスパムのフィルタ リング  <br/> |
|0x00000006  <br/> |低い迷惑メールのフィルタ リング  <br/> |
|0x00000003  <br/> |高い迷惑メールのフィルタ リング  <br/> |
|0x80000000  <br/> |リストのみ  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。
    
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
