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
ms.openlocfilehash: 152afd68bea44f3485b2cc566f3f0d2768590704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594475"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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

