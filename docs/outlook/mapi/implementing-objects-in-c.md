---
title: C 言語でオブジェクトを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d07d756abded137d3268daf7dd0998f0c953cb1d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563948"
---
# <a name="implementing-objects-in-c"></a>C 言語でオブジェクトを実装します。

**適用されます**: Outlook 2013 |Outlook 2016 
  
クライアント アプリケーションとサービス プロバイダーが C で書かれたデータ構造体と、仮想関数テーブルまたは vtable と呼ばれる順序付けられた関数ポインターの配列を作成することで MAPI オブジェクトを定義します。 Vtable へのポインターは、データ構造体の最初のメンバーである必要があります。
  
V のテーブル自体は、オブジェクトでサポートされている各インタ フェースのすべてのメソッドの 1 つのポインターがあります。 ポインターの順序は、Mapidefs.h ヘッダー ファイルで公開されているインターフェイスの仕様内のメソッドの順序に従う必要があります。 Vtable 内の各関数ポインターは、実際のメソッドの実装のアドレスに設定されています。 C++ では、コンパイラは、vtable を自動的に設定します。 C ではないです。 
  
次の図は、このしくみを示しています。 一番左のボックスでは、サービス プロバイダー オブジェクトを使用する必要があるクライアントを表します。 セッションでは、クライアントは、 **lpObject**オブジェクトへのポインターを取得します。 Vtable では、プライベート データとメソッドの後にオブジェクトの最初の項目が表示されます。 Vtable ポインターが指す実際の vtable は、の各インターフェイスのメソッドの実装へのポインターが含まれています。 
  
**オブジェクトの実装**
  
![オブジェクトの実装](media/amapi_42.gif "オブジェクトの実装")
  
C のサービス プロバイダーが、単純な状態のオブジェクトを定義する方法を次のコード例に示します。 最初のメンバーは、vtable ポインターです。オブジェクトの残りの部分はデータ メンバーで構成されています。 
  
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

それぞれのメソッドの実装へのポインターが vtable に含まれていますこのオブジェクトが状態オブジェクトであるため、 [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)の基本インターフェイスのメソッドの実装へのポインターと同様に、インターフェイス、IUnknown の**** と**IMAPIProp**。 Vtable 内のメソッドの順序は、Mapidefs.h ヘッダー ファイルで定義されている指定された順序と一致します。
  
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

クライアントとサービス プロバイダーが C で書かれた、v テーブルを通じて間接的にオブジェクトを使用し、すべての呼び出しの最初のパラメーターとして、オブジェクトのポインターを追加します。 MAPI インターフェイスのメソッドを呼び出すたびには、最初のパラメーターとして呼び出されているオブジェクトへのポインターが必要です。 C++ では、この目的のため、 **this**ポインターと呼ばれる特殊なポインターを定義します。 **This**ポインターは、最初のパラメーターとしてメソッド呼び出しのたびに、C++ コンパイラによって暗黙に追加します。 C ではこのようなポインターです。それを明示的に追加する必要があります。 
  
次のコードでは、クライアントが MYSTATUSOBJECT のインスタンスへの呼び出しを作成する方法を示します。
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>関連項目

- [MAPI オブジェクトの実装](implementing-mapi-objects.md)

