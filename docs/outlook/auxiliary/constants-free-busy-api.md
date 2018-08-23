---
title: 定数 (空き時間情報の API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: このトピックには、空き/予約済み API の定数の定義、クラス識別子とインターフェイス識別子が含まれています。
ms.openlocfilehash: ec909d449dc9075959fc9c047457577efd52ec3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799309"
---
# <a name="constants-freebusy-api"></a>定数 (空き時間情報の API)

このトピックには、空き/予約済み API の定数の定義、クラス識別子とインターフェイス識別子が含まれています。
  
## <a name="constants"></a>定数

|**定数**|**定義**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *ように Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル winerror.h で定義されています。*  <br/> |
|E_OUTOFMEMORY  <br/> | *ように Windows SDK のヘッダー ファイル winerror.h で定義されています。*  <br/> |
|S_FALSE  <br/> | *ように Windows SDK のヘッダー ファイル winerror.h で定義されています。*  <br/> |
|S_OK  <br/> | *ように Windows SDK のヘッダー ファイル winerror.h で定義されています。*  <br/> |
   
## <a name="interface-identifiers"></a>インターフェイス識別子

次のインターフェイス識別子は、DEFINE_GUID マクロの値で GUID のシンボリック名を関連付けるには、Windows SDK ヘッダー ファイル guiddef.h に定義されていると仮定します。
  
{00067064-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IEnumFBBlock、0x00067064、0x0、0x0、0xc0、0x0、0x0、0x0、0x0、0x0、0x0、0x46)。
  
{00067066-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusyData、0x00067066、0x0、0x0、0xc0、0x0、0x0、0x0、0x0、0x0、0x0、0x46)。
  
{00067067-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusySupport、0x00067067、0x0、0x0、0xc0、0x0、0x0、0x0、0x0、0x0、0x0、0x46)。
  

