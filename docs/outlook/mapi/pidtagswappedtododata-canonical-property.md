---
title: PidTagSwappedToDoData の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: dedb60c5356e1dbb6d35f27372a09c152da0fed0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803621"
---
# <a name="pidtagswappedtododata-canonical-property"></a>PidTagSwappedToDoData の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ オブジェクトのフラグが設定された状態に影響しないプロパティの値の 2 番目のセットを保持します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|識別子:  <br/> |0x0E2D  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>備考

フラグの送信者または送信者のアラームがサポートされている場合は、フラグをセカンダリ ・ ストレージの場所として機能している、この構造体はすべての送信者のフラグでサポートされている情報のフラグを設定するプロトコルに関連するプロパティとそのすべてを格納するための場所を提供します。送信者フラグまたはメッセージの受信者に送信者の通知情報を公開することがなく、送信者の通知でサポートされているアラームの設定のプロトコルに関連するプロパティ。
  
同様に、この構造体を提供するすべての受信者のフラグでサポートされている情報のフラグを設定するプロトコルに関連するプロパティおよび受信者でサポートされているアラームの設定のプロトコルに関連するプロパティを格納するための以前に送信されたメッセージで通知します。
  
このプロパティの詳細については、 [[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> 電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。
    
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

