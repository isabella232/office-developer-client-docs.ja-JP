---
title: PidLidWorkAddress の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidWorkAddress
api_type:
- COM
ms.assetid: fc3c0ab3-6920-4e82-bc69-6c083159628f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0ea3e2f88b3e0df2f358894cdf604dda651821b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802285"
---
# <a name="pidlidworkaddress-canonical-property"></a>PidLidWorkAddress の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
作業を終えたら、連絡先のアドレスを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidWorkAddress  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x0000801B  <br/> |
|データを入力します。  <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、他の物理アドレスのプロパティの組み合わせをする必要があり、クライアントのロケールに基づきます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
