---
title: C++ でオブジェクトを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4c233f9855674080496b2e54ba9548a53738ead8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574728"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="ab1af-103">C++ でオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="ab1af-103">Implementing objects in C++</span></span>

<span data-ttu-id="ab1af-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab1af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab1af-105">C++ クライアントおよびサービス ・ プロバイダーは、それらを実装しているインターフェイスから継承するクラスを作成することで MAPI オブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="ab1af-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="ab1af-106">クラスのデストラクターとコンス トラクターは、インターフェイスのメソッドはパブリックで。</span><span class="sxs-lookup"><span data-stu-id="ab1af-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="ab1af-107">クラスは、追加のメソッドを持っている場合、パブリックまたはプライベートの実装によって、できます。</span><span class="sxs-lookup"><span data-stu-id="ab1af-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="ab1af-108">すべてのデータ メンバーは、プライベートです。</span><span class="sxs-lookup"><span data-stu-id="ab1af-108">All data members are private.</span></span> 
  
<span data-ttu-id="ab1af-109">次のコード例では、C++ の状態オブジェクトを定義する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ab1af-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="ab1af-110">`CMyMAPIObject`クラスから継承、 [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="ab1af-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="ab1af-111">この例で使用されているマクロの多くは、OLE ヘッダー ファイル Compobj.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="ab1af-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="ab1af-112">クラスの最初のメンバーは、継承の順序で継承されたインターフェイスのメソッドの後に、基本インターフェイスのメソッドです。</span><span class="sxs-lookup"><span data-stu-id="ab1af-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="ab1af-113">追加のメソッド、コンス トラクター、デストラクター、およびデータ メンバーには次のインターフェイス定義です。</span><span class="sxs-lookup"><span data-stu-id="ab1af-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
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

<span data-ttu-id="ab1af-114">インスタンスを使用して、`CMyMAPIObject`クラス、C++ クライアントまたはサービス プロバイダーのメソッドのいずれかの呼び出しを行う次のようにします。</span><span class="sxs-lookup"><span data-stu-id="ab1af-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="ab1af-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab1af-115">See also</span></span>

- [<span data-ttu-id="ab1af-116">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="ab1af-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

