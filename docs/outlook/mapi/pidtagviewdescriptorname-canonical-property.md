---
title: PidTagViewDescriptorName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagViewDescriptorName
api_type:
- COM
ms.assetid: 1e689ee4-9e89-4328-beb9-05c80a6544a0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7cb5f25e9e9c4dc26998d164b0450ea5443f61bf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550282"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a>PidTagViewDescriptorName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ビュー記述子の名前が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_VD_NAME、PR_VD_NAME_A、PR_VD_NAME_W  <br/> |
|識別子:  <br/> |0x7006  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージ クラス定義の送信可能  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、ビュー定義を含むフォルダー関連情報 (FAI) メッセージの空でない文字列に設定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> 共有カテゴリ リストや作業時間など、クライアントおよびサーバー構成データの場所とプロパティを指定します。
    
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

