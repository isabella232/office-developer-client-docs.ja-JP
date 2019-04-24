---
title: PidTagResourcePath 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330171"
---
# <a name="pidtagresourcepath-canonical-property"></a>PidTagResourcePath 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービスプロバイダーのサーバーへのパスが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOURCE_PATH、PR_RESOURCE_PATH_A、PR_RESOURCE_PATH_W  <br/> |
|識別子:  <br/> |0x3e07  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティに含まれるパスは、ユーザーがリソースを検索できる、推奨されるパスを表します。 これらのプロパティの定義は、プロバイダーに固有のものです。 たとえば、スケジュールアプリケーションは、これらのプロパティを使用して、スケジューリングアプリケーションファイルに推奨される場所を指定します。
  
メッセージングユーザープロファイルは、これらのプロパティを利便性として furnishes するので、クライアントアプリケーションは、ネットワークパスまたはネットワークドライブ文字の入力を要求する必要はありません。
  
MAPI は、米国規格協会 (ANSI) 文字セットのファイル名に対してのみ機能します。 OEM (相手先ブランド供給) 文字セットでファイル名を使用するアプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

