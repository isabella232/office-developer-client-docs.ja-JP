---
title: PidTagProviderSubmitTime の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderSubmitTime
api_type:
- COM
ms.assetid: 9e5161d9-fefe-4a12-b7f7-5600f1d2e95b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 162451d000c0b3da42c8fbef5f64459bc5ae23b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803223"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a>PidTagProviderSubmitTime の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
トランスポート プロバイダーでは、その基になるメッセージング システムにメッセージが渡されるときの日時が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_PROVIDER_SUBMIT_TIME  <br/> |
|識別子:  <br/> |0x0048  <br/> |
|データを入力します。  <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、メッセージの送信時に送信トランスポート プロバイダーによって設定が。
  
このプロパティは、X.400 送信エンベロープ メッセージごとの属性に対応します。 
  
## <a name="related-resources"></a>関連リソース

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

