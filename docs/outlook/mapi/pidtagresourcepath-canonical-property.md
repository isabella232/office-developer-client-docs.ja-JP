---
title: PidTagResourcePath 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 04ecec1e220af4afcf40fe37fe5e3d90cf943720
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599601"
---
# <a name="pidtagresourcepath-canonical-property"></a>PidTagResourcePath 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーのサーバーへのパスを含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOURCE_PATH、PR_RESOURCE_PATH_A、PR_RESOURCE_PATH_W  <br/> |
|識別子:  <br/> |0x3E07  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティに含まれるパスは、ユーザーがリソースを検索できる推奨パスを表します。 これらのプロパティの定義はプロバイダー固有です。 たとえば、スケジュール アプリケーションは、これらのプロパティを使用して、スケジュール アプリケーション ファイルの推奨場所を指定します。
  
メッセージング ユーザー プロファイルは、クライアント アプリケーションがメッセージング ユーザーにネットワーク パスまたはネットワーク ドライブ文字の入力を求める必要が生じないので、これらのプロパティを便利に提供します。
  
MAPI は、米国国立標準研究所 (ANSI) の文字セットのファイル名でのみ動作します。 元の機器メーカー (OEM) の文字セットでファイル名を使用するアプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。
  
## <a name="related-resources"></a>関連リソース

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

