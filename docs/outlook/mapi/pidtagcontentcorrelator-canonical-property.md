---
title: PidTagContentCorrelator 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: baad9a247687f9753a5c63d27c7e9cdc07b74e5e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616545"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a>PidTagContentCorrelator 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ送信者がレポートと元のメッセージを一致するために使用できる値を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTENT_CORRELATOR  <br/> |
|識別子:  <br/> |0x0007  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>注釈

バイナリ文字列の内容は、メッセージの発信元によって定義されます。 送信メッセージに設定されている場合、このプロパティは、メッセージに応答して生成されたレポートにコピーする必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

