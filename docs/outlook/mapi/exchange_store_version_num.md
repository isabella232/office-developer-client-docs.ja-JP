---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 00d92f8e2ec3af766d5b241d1a911be304b346d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800017"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**適用対象**: Outlook 
  
Microsoft Office Outlook プロファイル内のアカウントが接続されている Microsoft Exchange Server のバージョン情報を格納します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a>Members

 _wMajorVersion_
  
- リリースの機能に重要な新機能と変更が含まれる場合、一般に増加するメジャー バージョン番号です。
    
 _wMinorVersion_
  
- マイナー バージョン番号が特定のメジャー バージョン番号に対応して、リリースには、マイナーの新機能や重要な修正が含まれている場合が一般的に増加します。
    
 _wBuild_
  
- メジャー ビルド番号が特定のメジャーおよびマイナー バージョン番号に対応して、新機能や修正プログラムを含む内部のリリースでは一般にインクリメントされます。 リリースの主要な内部コードの分岐、またはマイルス トーンのリリース候補などときにも、この値がインクリメントされます。
    
 _wMinorBuild_
  
- 内部リリースの新機能が含まれていますまたは主要なコードの分岐、またはマイルス トーンを示す特定の主要なビルドに対応する修正プログラムで一般に増加するマイナー ビルド番号です。
    
## <a name="see-also"></a>関連項目



[MAPI の追加について](about-mapi-additions.md)
  
[PidTagProfileServerFullVersion 標準プロパティ](pidtagprofileserverfullversion-canonical-property.md)

