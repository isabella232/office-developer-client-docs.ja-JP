---
title: MAPI フォーム サーバーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420767"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="f6573-103">MAPI フォーム サーバーの開発</span><span class="sxs-lookup"><span data-stu-id="f6573-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="f6573-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6573-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6573-105">このセクションでは、カスタム MAPI フォームを作成するためのフォーム サーバー実行可能ファイルとフォーム構成ファイルを作成するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f6573-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="f6573-106">このセクションを読む前に、MAPI フォームの情報を [理解する必要があります](mapi-forms.md)。</span><span class="sxs-lookup"><span data-stu-id="f6573-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="f6573-107">フォーム サーバーの開発には、次の手順が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f6573-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="f6573-108">フォームに含まれる情報を決定し、その情報を保持する一連のプロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="f6573-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="f6573-109">詳細については、「フォームの [プロパティ セットの選択」を参照してください](choosing-a-form-s-property-set.md)。</span><span class="sxs-lookup"><span data-stu-id="f6573-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="f6573-110">ユーザーがフォームのプロパティを操作できるユーザー インターフェイスを設計する。</span><span class="sxs-lookup"><span data-stu-id="f6573-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="f6573-111">メッセージ クラスを選択し、一意のクラス識別子 (CLSID) を生成します。</span><span class="sxs-lookup"><span data-stu-id="f6573-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="f6573-112">メッセージ クラスの概要については、「MAPI メッセージ [クラス」を参照してください](mapi-message-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="f6573-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="f6573-113">メッセージ クラスとフォームの詳細については、「 [メッセージ クラスの選択」を参照してください](choosing-a-message-class.md)。</span><span class="sxs-lookup"><span data-stu-id="f6573-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="f6573-114">必要な MAPI フォーム インターフェイスと、特定のフォーム サーバーが必要とする任意のオプション インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="f6573-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="f6573-115">詳細については、「フォーム サーバー コードの [記述」を参照してください](writing-form-server-code.md)。</span><span class="sxs-lookup"><span data-stu-id="f6573-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="f6573-116">フォーム オブジェクトとフォームが使用するプロパティとのユーザーのやり取りを処理するユーザー インターフェイス コードを記述します。</span><span class="sxs-lookup"><span data-stu-id="f6573-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="f6573-117">フォームのフォーム構成ファイルの作成。</span><span class="sxs-lookup"><span data-stu-id="f6573-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="f6573-118">詳細については、「フォーム構成 [ファイルのファイル形式」を参照してください](file-format-of-form-configuration-files.md)。</span><span class="sxs-lookup"><span data-stu-id="f6573-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="f6573-119">ユーザーのコンピューターにフォームをインストールする。</span><span class="sxs-lookup"><span data-stu-id="f6573-119">Installing the form on users' computers.</span></span> <span data-ttu-id="f6573-120">詳細については、「ライブラリへの [フォームのインストール」を参照してください](installing-a-form-into-a-library.md)。</span><span class="sxs-lookup"><span data-stu-id="f6573-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="f6573-121">手順 1 ~ 5 を同時に実行する場合は、手順 1 ~ 5 を順に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6573-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="f6573-122">フォーム サーバーを開発するプロセスは、多くのプログラミング プロジェクトと同様に、特に定義されたシーケンスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f6573-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="f6573-123">たとえば、フォーム構成ファイルの作成は上記の 2 番目から最後の手順として表示されますが、フォーム構成ファイルは段階的に作成され、フォーム サーバーに機能を追加するほど完全になります。</span><span class="sxs-lookup"><span data-stu-id="f6573-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f6573-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6573-124">See also</span></span>



[<span data-ttu-id="f6573-125">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="f6573-125">MAPI Concepts</span></span>](mapi-concepts.md)

