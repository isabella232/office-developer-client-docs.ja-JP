---
title: 定数 (空き時間情報 API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: このトピックでは、空き時間情報 API の定数の定義、クラス識別子、およびインターフェイス識別子について説明します。
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431534"
---
# <a name="constants-freebusy-api"></a>定数 (空き時間情報 API)

このトピックでは、空き時間情報 API の定数の定義、クラス識別子、およびインターフェイス識別子について説明します。
  
## <a name="constants"></a>定数

|**定数**|**定義**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *Microsoft Windows Software Development Kit (SDK) ヘッダーファイル winerror.h で定義されています。*  <br/> |
|E_OUTOFMEMORY  <br/> | *Windows SDK ヘッダーファイル winerror.h で定義されています。*  <br/> |
|S_FALSE  <br/> | *Windows SDK ヘッダーファイル winerror.h で定義されています。*  <br/> |
|S_OK  <br/> | *Windows SDK ヘッダーファイル winerror.h で定義されています。*  <br/> |
   
## <a name="interface-identifiers"></a>インターフェイス識別子

次のインターフェイス識別子の場合、Windows SDK ヘッダーファイル guiddef で定義されている DEFINE_GUID マクロを使用して、GUID シンボリック名とその値を関連付けます。
  
{00067064-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IEnumFBBlock、0x00067064、0x0、0x0、0xc0、0x0、0x0、0x0、0x0、0x0、0x0、0x46);
  
{00067066-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusyData、0x00067066、0x0、0x0、0xc0、0x0、0x0、0x0、0x0、0x0、0x0、0x46);
  
{00067067-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusySupport、0x00067067、0x0、0x0、0xc0、0x0、0x0、0x0、0x0、0x0、0x0、0x46);
  

