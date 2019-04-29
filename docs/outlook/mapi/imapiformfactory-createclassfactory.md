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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6e616a76d9665b602184e88566384506fcce5697
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416077"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="306e4-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="306e4-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="306e4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="306e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="306e4-105">フォームのクラスファクトリオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="306e4-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="306e4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="306e4-106">Parameters</span></span>

 <span data-ttu-id="306e4-107">_clsidform_</span><span class="sxs-lookup"><span data-stu-id="306e4-107">_clsidForm_</span></span>
  
> <span data-ttu-id="306e4-108">順番クラスファクトリによって作成されるフォームのクラス識別子。</span><span class="sxs-lookup"><span data-stu-id="306e4-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="306e4-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="306e4-109">_ulFlags_</span></span>
  
> <span data-ttu-id="306e4-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="306e4-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="306e4-111">_lppclassfactory_</span><span class="sxs-lookup"><span data-stu-id="306e4-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="306e4-112">読み上げクラスファクトリオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="306e4-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="306e4-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="306e4-113">Return value</span></span>

<span data-ttu-id="306e4-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="306e4-114">S_OK</span></span> 
  
> <span data-ttu-id="306e4-115">クラスファクトリオブジェクトが返されました。</span><span class="sxs-lookup"><span data-stu-id="306e4-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="306e4-116">注釈</span><span class="sxs-lookup"><span data-stu-id="306e4-116">Remarks</span></span>

<span data-ttu-id="306e4-117">フォーム閲覧者は、 **imapiformfactory:: CreateClassFactory**メソッドを呼び出して、特定のフォームのクラスファクトリを取得します。</span><span class="sxs-lookup"><span data-stu-id="306e4-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="306e4-118">クラスファクトリは、特定のクラスのメッセージを処理するフォームのインスタンスを作成し、それらのインスタンスへのアクセスを制御するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="306e4-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="306e4-119">**CreateClassFactory**メソッドは、フォームビューアーによって呼び出され、複数のメッセージクラスを実装するフォームサーバーのクラスファクトリオブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="306e4-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="306e4-120">このメソッドは、クラス識別子 (CLSID) をパラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="306e4-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="306e4-121">このパラメーターに基づいて、このメソッドは、返される特定の種類のクラスファクトリオブジェクトを決定できます。</span><span class="sxs-lookup"><span data-stu-id="306e4-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="306e4-122">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="306e4-122">Notes to implementers</span></span>

<span data-ttu-id="306e4-123">同じクラス識別子に対する複数の呼び出しで、 **CreateClassFactory**実装から同じクラスファクトリオブジェクトを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="306e4-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="306e4-124">新しいクラスファクトリインスタンスを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="306e4-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="306e4-125">必要に応じて適切なクラスファクトリインスタンスを作成するか、メッセージクラスごとに1つずつ、複数のクラスファクトリの実装を作成する、単一のクラスファクトリ実装を使用できます。</span><span class="sxs-lookup"><span data-stu-id="306e4-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="306e4-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="306e4-126">See also</span></span>



[<span data-ttu-id="306e4-127">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="306e4-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

