---
title: C++ でのオブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 89247ca1b263d6f06af73f1ffa14709a2aff23de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310151"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="61888-103">C++ でのオブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="61888-103">Implementing objects in C++</span></span>

<span data-ttu-id="61888-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61888-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61888-105">C++ クライアントおよびサービスプロバイダーは、実装するインターフェイスから継承するクラスを作成することによって、MAPI オブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="61888-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="61888-106">各インターフェイスメソッドは、クラスのコンストラクターおよびデストラクターとして、public になります。</span><span class="sxs-lookup"><span data-stu-id="61888-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="61888-107">クラスに追加のメソッドがある場合は、実装に応じてパブリックまたはプライベートにすることができます。</span><span class="sxs-lookup"><span data-stu-id="61888-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="61888-108">すべてのデータメンバーがプライベートである。</span><span class="sxs-lookup"><span data-stu-id="61888-108">All data members are private.</span></span> 
  
<span data-ttu-id="61888-109">次のコード例は、C++ status オブジェクトを定義する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="61888-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="61888-110">クラス`CMyMAPIObject`は[imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイスから継承します。</span><span class="sxs-lookup"><span data-stu-id="61888-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="61888-111">この例で使用されているマクロの多くは、OLE ヘッダーファイル compobj で定義されています。</span><span class="sxs-lookup"><span data-stu-id="61888-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="61888-112">クラスの最初のメンバーは、基本インターフェイスのメソッドです。その後に、継承されたインターフェイスのメソッドが継承順に続きます。</span><span class="sxs-lookup"><span data-stu-id="61888-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="61888-113">インターフェイス定義の後には、追加のメソッド、コンストラクターとデストラクター、データメンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="61888-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
```cpp
class  CMyMAPIObject : public IMAPIStatus
{
public:
// Methods of IUnknown.
    STDMETHODIMP QueryInterface (REFIID riid, LPVOID * ppvObj);
    STDMETHODIMP_(ULONG) AddRef ();
    STDMETHODIMP_(ULONG) Release ();
    MAPI_IMAPIPROP_METHODS(IMPL);
    MAPI_IMAPISTATUS_METHODS(IMPL);
// Other methods specific to CMyMAPIObject.
    BOOL WINAPI Method1 ();
    void WINAPI Method2 ();
// Constructors and destructors.
public :
    CMyMAPIObject () {};
    ~CMyMAPIObject () {};
// Data members specific to CMyMAPIObject.
private :
    ULONG               m_cRef;
    CAnotherObj *       m_pObj;
};
 
```

<span data-ttu-id="61888-114">`CMyMAPIObject`クラスのインスタンスを使用するために、C++ クライアントまたはサービスプロバイダーは、次のように、そのメソッドのいずれかに呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="61888-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="61888-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="61888-115">See also</span></span>

- [<span data-ttu-id="61888-116">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="61888-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

