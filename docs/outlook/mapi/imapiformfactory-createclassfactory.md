---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 823e10a1f496f5f5e8bab00f94d700d06e753b48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800547"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="804ab-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="804ab-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="804ab-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="804ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="804ab-105">フォームのクラス ファクトリ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="804ab-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="804ab-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="804ab-106">Parameters</span></span>

 <span data-ttu-id="804ab-107">_clsidForm_</span><span class="sxs-lookup"><span data-stu-id="804ab-107">_clsidForm_</span></span>
  
> <span data-ttu-id="804ab-108">[in]クラス ファクトリによって作成されるフォームのクラス識別子です。</span><span class="sxs-lookup"><span data-stu-id="804ab-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="804ab-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="804ab-109">_ulFlags_</span></span>
  
> <span data-ttu-id="804ab-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="804ab-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="804ab-111">_lppClassFactory_</span><span class="sxs-lookup"><span data-stu-id="804ab-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="804ab-112">[out]クラス ファクトリ オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="804ab-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="804ab-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="804ab-113">Return value</span></span>

<span data-ttu-id="804ab-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="804ab-114">S_OK</span></span> 
  
> <span data-ttu-id="804ab-115">クラス ファクトリ オブジェクトが返されました。</span><span class="sxs-lookup"><span data-stu-id="804ab-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="804ab-116">備考</span><span class="sxs-lookup"><span data-stu-id="804ab-116">Remarks</span></span>

<span data-ttu-id="804ab-117">フォーム ビューアーは、特定のフォームのクラス ファクトリを取得する**IMAPIFormFactory::CreateClassFactory**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="804ab-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="804ab-118">クラス ファクトリは、特定のクラスのメッセージを処理するフォームのインスタンスを作成して、これらのインスタンスへのアクセスを制御するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="804ab-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="804ab-119">**CreateClassFactory**メソッドは、複数のメッセージ クラスを実装しているフォームのサーバーのクラス ファクトリ オブジェクトを取得するフォーム ビューアーによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="804ab-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="804ab-120">このメソッドは、クラス識別子 (CLSID) をパラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="804ab-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="804ab-121">そのパラメーターに基づいて、このメソッドは、返されるクラス ファクトリ オブジェクトの特定の種類を決定できます。</span><span class="sxs-lookup"><span data-stu-id="804ab-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="804ab-122">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="804ab-122">Notes to implementers</span></span>

<span data-ttu-id="804ab-123">オブジェクトを取得できます、 **CreateClassFactory**の実装から、同じクラス工場出荷時に同じ識別子がクラスの複数の呼び出し。</span><span class="sxs-lookup"><span data-stu-id="804ab-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="804ab-124">クラス ファクトリの新しいインスタンスを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="804ab-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="804ab-125">1 つのクラス ファクトリの実装を必要に応じて、適切なクラス ファクトリのインスタンスを作成するか、複数のクラス ファクトリ実装は、各メッセージ クラスの 1 つを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="804ab-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="804ab-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="804ab-126">See also</span></span>



[<span data-ttu-id="804ab-127">IMAPIFormFactory: IUnknown</span><span class="sxs-lookup"><span data-stu-id="804ab-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

