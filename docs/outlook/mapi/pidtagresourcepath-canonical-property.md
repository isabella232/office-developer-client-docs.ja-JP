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
ms.openlocfilehash: d7385ea403e7ea45c97f6fd98e422ad7eb762c4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803358"
---
# <a name="pidtagresourcepath-canonical-property"></a>PidTagResourcePath 標準プロパティ

  
  
**適用対象**: Outlook 
  
サービス プロバイダーのサーバーへのパスが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOURCE_PATH、PR_RESOURCE_PATH_A、PR_RESOURCE_PATH_W  <br/> |
|識別子:  <br/> |0x3E07  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティに含まれているパスは、ユーザーがリソースを検索する場所として推奨されるパスを表します。 これらのプロパティの定義は、特定のプロバイダーです。 などのスケジュール アプリケーションは、そのスケジュールのアプリケーション ファイルの推奨される場所を指定するのにこれらのプロパティを使用します。
  
メッセージングのユーザー プロファイルは、クライアント アプリケーションが、ネットワーク パスまたはネットワーク ドライブの文字のメッセージのユーザーに確認する必要があるないように、必要に応じてこれらのプロパティを提供します。
  
MAPI は、米国規格協会 (ANSI) 文字セットのファイル名でのみ動作します。 正規機器製造元 (OEM) 文字セットでファイル名を使用するアプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。
  
## <a name="related-resources"></a>関連リソース

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

