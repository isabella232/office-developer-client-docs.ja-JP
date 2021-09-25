---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 59f3034fa4217f3ee43cda959e07fd0bc9f8f784
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551647"
---
# <a name="exchange_store_version_num"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルが接続されているアカウントMicrosoft Exchange Serverのバージョン情報Microsoft Office Outlook格納します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a>メンバー

 _wMajorVersion_
  
- リリースに大幅な新機能と機能の変更が含まれている場合に一般的に増分されるメジャー バージョン番号。
    
 _wMinorVersion_
  
- 特定のメジャー バージョン番号に対応するマイナー バージョン番号で、リリースにマイナーな新機能や大幅な修正が含まれている場合、通常は増分されます。
    
 _wBuild_
  
- 特定のメジャー バージョン番号とマイナー バージョン番号に対応し、一般に、新機能または修正プログラムを含む内部リリースで増分されるメジャー ビルド番号。 この値は、リリースが主要な内部コードブランチまたはマイルストーン (リリース候補など) である場合にも増分されます。
    
 _wMinorBuild_
  
- メジャー コードブランチまたはマイルストーンを表す特定のメジャー ビルドに対応する新機能または修正プログラムを含む内部リリースで一般的に増分されるマイナービルド番号。
    
## <a name="see-also"></a>関連項目



[MAPI の追加について](about-mapi-additions.md)
  
[PidTagProfileServerFullVersion 標準プロパティ](pidtagprofileserverfullversion-canonical-property.md)

