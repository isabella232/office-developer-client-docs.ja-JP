---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf60b12a6e4575d3504a112aa2b54fb8c4ae23c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433725"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
microsoft Office Outlook プロファイルのアカウントが接続されている microsoft Exchange Server のバージョン情報を格納します。
  
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

 _wmajorversion_
  
- リリースに重要な新機能と機能の変更が含まれている場合に、通常はメジャーバージョン番号がインクリメントされます。
    
 _wMinorVersion_
  
- 特定のメジャーバージョン番号に対応するマイナーバージョン番号。リリースにマイナーな新機能や重要な修正が含まれている場合に、通常は増分されます。
    
 _wbuild_
  
- 特定のメジャーおよびマイナーバージョン番号に対応し、新しい機能またはフィックスを含む内部リリースで一般的にインクリメントされるメジャービルド番号。 この値は、リリース候補のように、リリースが主要な内部コード分岐またはマイルストーンの場合にも増加します。
    
 _wminorbuild_
  
- メジャーコード分岐またはマイルストーンを示す、特定の主要ビルドに対応する新機能またはフィックスを含む内部リリースで通常増分されるマイナービルド番号。
    
## <a name="see-also"></a>関連項目



[MAPI の追加について](about-mapi-additions.md)
  
[PidTagProfileServerFullVersion 標準プロパティ](pidtagprofileserverfullversion-canonical-property.md)

