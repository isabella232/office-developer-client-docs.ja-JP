---
title: C でのオブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6026e697cc31545bf7ef518fcbd33ea8db48af5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414943"
---
# <a name="implementing-objects-in-c"></a>C でのオブジェクトの実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
C で記述されたクライアント アプリケーションとサービス プロバイダーは、データ構造と、仮想関数テーブル (vtable) と呼ばれる順序付き関数ポインターの配列を作成して MAPI オブジェクトを定義します。 vtable へのポインターは、データ構造の最初のメンバーである必要があります。
  
vtable 自体には、オブジェクトでサポートされている各インターフェイスのすべてのメソッドに 1 つのポインターがあります。 ポインターの順序は、Mapidefs.h ヘッダー ファイルで公開されているインターフェイス仕様のメソッドの順序に従う必要があります。 vtable 内の各関数ポインターは、メソッドの実際の実装のアドレスに設定されます。 C++ では、コンパイラによって vtable が自動的にセットアップされます。 C では、そうではありません。 
  
次の図は、この動作を示しています。 左上のボックスは、サービス プロバイダー オブジェクトを使用する必要があるクライアントを表します。 セッションを通じて、クライアントはオブジェクト lpObject へのポインター **を取得します**。 vtable はオブジェクトの最初に表示され、その後にプライベート データとメソッドが続きます。 vtable ポインターは、インターフェイス内の各メソッドの実装へのポインターを含む実際の vtable を指します。 
  
**オブジェクトの実装**
  
![オブジェクト実装](media/amapi_42.gif "オブジェクトの実装")
  
次のコード例は、C サービス プロバイダーが単純な状態オブジェクトを定義する方法を示しています。 最初のメンバーは、vtable ポインターです。オブジェクトの残りの部分はデータ メンバーででなされます。 
  
```C
typedef struct _MYSTATUSOBJECT
{
    const STATUS_Vtbl FAR *lpVtbl;
    ULONG              cRef;
    ANOTHEROBJ        *pObj;
    LPMAPIPROP         lpProp;
    LPFREEBUFFER       lpFreeBuf;
} MYSTATUSOBJECT, *LPMYSTATUSOBJ;
 
```

このオブジェクトは状態オブジェクトなので、vtable には [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) インターフェイス内の各メソッドの実装へのポインターと、基本インターフェイスの各メソッドの実装へのポインター **(IUnknown** および **IMAPIProp)** が含まれます。 vtable 内のメソッドの順序は、Mapidefs.h ヘッダー ファイルで定義されている指定された順序と一致します。
  
```js
static const MYOBJECT_Vtbl vtblSTATUS =
{
    STATUS_QueryInterface,
    STATUS_AddRef,
    STATUS_Release,
    STATUS_GetLastError,
    STATUS_SaveChanges,
    STATUS_GetProps,
    STATUS_GetPropList,
    STATUS_OpenProperty,
    STATUS_SetProps,
    STATUS_DeleteProps,
    STATUS_CopyTo,
    STATUS_CopyProps,
    STATUS_GetNamesFromIDs,
    STATUS_GetIDsFromNames,
    STATUS_ValidateState,
    STATUS_SettingsDialog,
    STATUS_ChangePassword,
    STATUS_FlushQueues
};
 
```

C で記述されたクライアントとサービス プロバイダーは、vtable を介して間接的にオブジェクトを使用し、すべての呼び出しの最初のパラメーターとしてオブジェクト ポインターを追加します。 MAPI インターフェイス メソッドを呼び出すごとに、最初のパラメーターとして呼び出されるオブジェクトへのポインターが必要です。 C++ は、この目的のためにこのポインターと呼 **ばれる特別** なポインターを定義します。 C++ コンパイラは、このポインター **を最初** のパラメーターとしてすべてのメソッド呼び出しに暗黙的に追加します。 C では、そのようなポインターはありません。明示的に追加する必要があります。 
  
次のコードは、クライアントが MYSTATUSOBJECT のインスタンスを呼び出す方法を示しています。
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>関連項目

- [MAPI オブジェクトの実装](implementing-mapi-objects.md)

