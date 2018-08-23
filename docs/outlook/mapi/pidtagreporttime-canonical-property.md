---
title: PidTagReportTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTime
api_type:
- COM
ms.assetid: b3646505-a9f0-4a72-8277-b238c909f66f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4efe68745c10521de243677c10a9ca32debd7122
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577801"
---
# <a name="pidtagreporttime-canonical-property"></a>PidTagReportTime 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージング システムにレポートが生成されたときの日時が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_REPORT_TIME  <br/> |
|識別子:  <br/> |0x0032  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、配信し、配信不能レポートの受信者ごとのプロパティとレポートの読み取りと nonread のメッセージごとのプロパティを表します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージの許可の操作を指定します。
    
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
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

