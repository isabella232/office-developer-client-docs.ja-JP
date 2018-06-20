---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c1a78889ea98133af46089fdc93b0c1c4bb24226
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801546"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**適用されます**: Outlook 
  
、参照カウントのクリーンアップ処理をデクリメントし、削除インスタンスごとのグローバルなデータの MAPI DLL です。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>Parameters

なし 
  
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>備考

クライアント アプリケーションでは、[生じます](mapiinitialize.md)関数の呼び出しによって開始されている MAPI との対話を終了する**MAPIUninitialize**関数を呼び出します。 **MAPIUninitialize**が呼び出されると、その他の MAPI 呼び出し可能ないクライアントです。 
  
 **MAPIUninitialize**参照をデクリメント、および対応する**生じます**関数は、参照カウントをインクリメントします。 したがって、1 つの関数への呼び出しの数は、他の呼び出しの数に等しくなければなりません。 
  
> [!NOTE]
> Win32 **DllMain**関数またはその他の機能を作成するか、スレッドを終了するのには**生じます**かから**MAPIUninitialize**を呼び出すことはできません。 詳細については、[スレッド セーフであるオブジェクトを使用する](using-thread-safe-objects.md)を参照してください。 
  

