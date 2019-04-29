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
  
C で記述されたクライアントアプリケーションとサービスプロバイダーは、データ構造と、仮想関数テーブルまたは vtable と呼ばれる順序付き関数ポインターの配列を作成することによって、MAPI オブジェクトを定義します。 vtable へのポインターは、データ構造体の最初のメンバーである必要があります。
  
vtable 自体には、オブジェクトでサポートされている各インターフェイスのすべてのメソッドに対して1つのポインターがあります。 ポインターの順序は、mapidefs.h ヘッダーファイルで公開されているインターフェイス仕様のメソッドの順序に従う必要があります。 vtable 内の各関数ポインターは、メソッドの実際の実装のアドレスに設定されます。 C++ では、コンパイラは自動的に vtable を設定します。 C では、できません。 
  
次の図は、このしくみを示しています。 左端のボックスは、サービスプロバイダオブジェクトを使用する必要があるクライアントを表します。 セッションを通じて、クライアントは**lpObject**オブジェクトへのポインターを取得します。 最初に vtable がオブジェクトの先頭に表示され、その後にプライベートデータとメソッドが続きます。 vtable ポインターは、実際の vtable をポイントします。これには、インターフェイス内のメソッドの各実装へのポインターが含まれています。 
  
**オブジェクトの実装**
  
![オブジェクトの実装](media/amapi_42.gif "オブジェクトの実装")
  
次のコード例は、C サービスプロバイダーが簡単な status オブジェクトを定義する方法を示しています。 最初のメンバーは vtable ポインターです。オブジェクトの残りの部分は、データメンバーで構成されています。 
  
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

このオブジェクトは status オブジェクトなので、vtable には、 [imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイスの各メソッドの実装へのポインターと、基本インターフェイス内の各メソッドの実装へのポインターが含まれています。 **IUnknown**および**imapiprop**。 vtable 内のメソッドの順序は、mapidefs.h ヘッダーファイルで定義されている順序と一致します。
  
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

C で記述されたクライアントおよびサービスプロバイダーは、vtable を介して間接的にオブジェクトを使用し、すべての呼び出しの最初のパラメーターとしてオブジェクトポインターを追加します。 MAPI インターフェイスメソッドへのすべての呼び出しでは、最初のパラメーターとして呼び出されるオブジェクトへのポインターが必要です。 C++ では、この目的のために**this**ポインターとして知られている特殊なポインターを定義しています。 C++ コンパイラは、すべてのメソッド呼び出しに最初のパラメーターとして**この**ポインターを暗黙的に追加します。 C では、そのようなポインターはありません。明示的に追加する必要があります。 
  
次のコードは、クライアントが mystatusobject のインスタンスを呼び出す方法を示しています。
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>関連項目

- [MAPI オブジェクトの実装](implementing-mapi-objects.md)

