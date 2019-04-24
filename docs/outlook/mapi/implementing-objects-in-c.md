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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310191"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="e901e-103">C でのオブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="e901e-103">Implementing objects in C</span></span>

<span data-ttu-id="e901e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e901e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e901e-105">C で記述されたクライアントアプリケーションとサービスプロバイダーは、データ構造と、仮想関数テーブルまたは vtable と呼ばれる順序付き関数ポインターの配列を作成することによって、MAPI オブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="e901e-105">Client applications and service providers written in C define MAPI objects by creating a data structure and an array of ordered function pointers known as a virtual function table, or vtable.</span></span> <span data-ttu-id="e901e-106">vtable へのポインターは、データ構造体の最初のメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e901e-106">A pointer to the vtable must be the first member of the data structure.</span></span>
  
<span data-ttu-id="e901e-107">vtable 自体には、オブジェクトでサポートされている各インターフェイスのすべてのメソッドに対して1つのポインターがあります。</span><span class="sxs-lookup"><span data-stu-id="e901e-107">In the vtable itself, there is one pointer for every method in each interface supported by the object.</span></span> <span data-ttu-id="e901e-108">ポインターの順序は、mapidefs.h ヘッダーファイルで公開されているインターフェイス仕様のメソッドの順序に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e901e-108">The order of the pointers must follow the order of the methods in the interface specification published in the Mapidefs.h header file.</span></span> <span data-ttu-id="e901e-109">vtable 内の各関数ポインターは、メソッドの実際の実装のアドレスに設定されます。</span><span class="sxs-lookup"><span data-stu-id="e901e-109">Each function pointer in the vtable is set to the address of the actual implementation of the method.</span></span> <span data-ttu-id="e901e-110">C++ では、コンパイラは自動的に vtable を設定します。</span><span class="sxs-lookup"><span data-stu-id="e901e-110">In C++, the compiler automatically sets up the vtable.</span></span> <span data-ttu-id="e901e-111">C では、できません。</span><span class="sxs-lookup"><span data-stu-id="e901e-111">In C, it does not.</span></span> 
  
<span data-ttu-id="e901e-112">次の図は、このしくみを示しています。</span><span class="sxs-lookup"><span data-stu-id="e901e-112">The following illustration shows how this works.</span></span> <span data-ttu-id="e901e-113">左端のボックスは、サービスプロバイダオブジェクトを使用する必要があるクライアントを表します。</span><span class="sxs-lookup"><span data-stu-id="e901e-113">The box on the far left represents a client that needs to use a service provider object.</span></span> <span data-ttu-id="e901e-114">セッションを通じて、クライアントは**lpObject**オブジェクトへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="e901e-114">Through the session, the client obtains a pointer to the object, **lpObject**.</span></span> <span data-ttu-id="e901e-115">最初に vtable がオブジェクトの先頭に表示され、その後にプライベートデータとメソッドが続きます。</span><span class="sxs-lookup"><span data-stu-id="e901e-115">The vtable appears first in the object followed by private data and methods.</span></span> <span data-ttu-id="e901e-116">vtable ポインターは、実際の vtable をポイントします。これには、インターフェイス内のメソッドの各実装へのポインターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e901e-116">The vtable pointer points to the actual vtable, which contains pointers to each of the implementations of the methods in the interface.</span></span> 
  
<span data-ttu-id="e901e-117">**オブジェクトの実装**</span><span class="sxs-lookup"><span data-stu-id="e901e-117">**Object implementation**</span></span>
  
<span data-ttu-id="e901e-118">![オブジェクトの実装](media/amapi_42.gif "オブジェクトの実装")</span><span class="sxs-lookup"><span data-stu-id="e901e-118">![Object implementation](media/amapi_42.gif "Object implementation")</span></span>
  
<span data-ttu-id="e901e-119">次のコード例は、C サービスプロバイダーが簡単な status オブジェクトを定義する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e901e-119">The following code example shows how a C service provider can define a simple status object.</span></span> <span data-ttu-id="e901e-120">最初のメンバーは vtable ポインターです。オブジェクトの残りの部分は、データメンバーで構成されています。</span><span class="sxs-lookup"><span data-stu-id="e901e-120">The first member is the vtable pointer; the rest of the object is made up of data members.</span></span> 
  
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

<span data-ttu-id="e901e-121">このオブジェクトは status オブジェクトなので、vtable には、 [imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイスの各メソッドの実装へのポインターと、基本インターフェイス内の各メソッドの実装へのポインターが含まれています。 **IUnknown**および**imapiprop**。</span><span class="sxs-lookup"><span data-stu-id="e901e-121">Because this object is a status object, the vtable includes pointers to implementations of each of the methods in the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, as well as pointers to implementations of each of the methods in the base interfaces — **IUnknown** and **IMAPIProp**.</span></span> <span data-ttu-id="e901e-122">vtable 内のメソッドの順序は、mapidefs.h ヘッダーファイルで定義されている順序と一致します。</span><span class="sxs-lookup"><span data-stu-id="e901e-122">The order of methods in the vtable matches the specified order as defined in the Mapidefs.h header file.</span></span>
  
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

<span data-ttu-id="e901e-123">C で記述されたクライアントおよびサービスプロバイダーは、vtable を介して間接的にオブジェクトを使用し、すべての呼び出しの最初のパラメーターとしてオブジェクトポインターを追加します。</span><span class="sxs-lookup"><span data-stu-id="e901e-123">Clients and service providers written in C use objects indirectly through the vtable and add an object pointer as the first parameter in every call.</span></span> <span data-ttu-id="e901e-124">MAPI インターフェイスメソッドへのすべての呼び出しでは、最初のパラメーターとして呼び出されるオブジェクトへのポインターが必要です。</span><span class="sxs-lookup"><span data-stu-id="e901e-124">Every call to a MAPI interface method requires a pointer to the object being called as its first parameter.</span></span> <span data-ttu-id="e901e-125">C++ では、この目的のために**this**ポインターとして知られている特殊なポインターを定義しています。</span><span class="sxs-lookup"><span data-stu-id="e901e-125">C++ defines a special pointer known as the **this** pointer for this purpose.</span></span> <span data-ttu-id="e901e-126">C++ コンパイラは、すべてのメソッド呼び出しに最初のパラメーターとして**この**ポインターを暗黙的に追加します。</span><span class="sxs-lookup"><span data-stu-id="e901e-126">The C++ compiler implicitly adds the **this** pointer as the first parameter to every method call.</span></span> <span data-ttu-id="e901e-127">C では、そのようなポインターはありません。明示的に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e901e-127">In C there is no such pointer; it must be explicitly added.</span></span> 
  
<span data-ttu-id="e901e-128">次のコードは、クライアントが mystatusobject のインスタンスを呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e901e-128">The following code demonstrates how a client can make a call to an instance of MYSTATUSOBJECT:</span></span>
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a><span data-ttu-id="e901e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e901e-129">See also</span></span>

- [<span data-ttu-id="e901e-130">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="e901e-130">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

