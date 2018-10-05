---
title: PidTagSwappedToDoData 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386671"
---
# <a name="pidtagswappedtododata-canonical-property"></a>PidTagSwappedToDoData 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ オブジェクトのフラグが設定された状態に影響しないプロパティの値の 2 番目のセットを保持します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|識別子:  <br/> |0x0E2D  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>備考

フラグの送信者または送信者のアラームがサポートされている場合は、フラグをセカンダリ ・ ストレージの場所として機能している、この構造体はすべての送信者のフラグでサポートされている情報のフラグを設定するプロトコルに関連するプロパティとそのすべてを格納するための場所を提供します。送信者フラグまたはメッセージの受信者に送信者の通知情報を公開することがなく、送信者の通知でサポートされているアラームの設定のプロトコルに関連するプロパティ。
  
同様に、この構造体を提供するすべての受信者のフラグでサポートされている情報のフラグを設定するプロトコルに関連するプロパティおよび受信者でサポートされているアラームの設定のプロトコルに関連するプロパティを格納するための以前に送信されたメッセージで通知します。
  
このプロパティの詳細については、 [[MS OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
[[MS OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> 電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。
    
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

