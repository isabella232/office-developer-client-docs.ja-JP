---
title: MAPI フォームのサーバーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 83d652f313e139b1c6bb628d1119edda03a70e23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799920"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="e9492-103">MAPI フォームのサーバーの開発</span><span class="sxs-lookup"><span data-stu-id="e9492-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="e9492-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9492-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9492-105">このセクションでは、フォーム サーバーの実行可能ファイルとカスタム MAPI フォームを作成するためのフォーム構成ファイルを作成するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e9492-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="e9492-106">このセクションを読む前にする必要があります理解する[MAPI フォーム](mapi-forms.md)内の情報です。</span><span class="sxs-lookup"><span data-stu-id="e9492-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="e9492-107">フォームのサーバーを開発すると、次の手順が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e9492-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="e9492-108">フォームに含まれるどのような情報を決定して、その情報を保持するプロパティのセットを選択します。</span><span class="sxs-lookup"><span data-stu-id="e9492-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="e9492-109">詳細については、[フォームのプロパティの設定を選択する](choosing-a-form-s-property-set.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9492-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="e9492-110">フォームのプロパティを持つユーザーが対話するユーザー インターフェイスを設計しています。</span><span class="sxs-lookup"><span data-stu-id="e9492-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="e9492-111">メッセージ クラスを選択し、一意のクラス識別子 (CLSID) を生成しています。</span><span class="sxs-lookup"><span data-stu-id="e9492-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="e9492-112">メッセージ クラスの概要については、 [MAPI メッセージ クラス](mapi-message-classes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9492-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="e9492-113">メッセージ クラスおよびフォームの詳細については、[メッセージ クラスを選択する](choosing-a-message-class.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9492-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="e9492-114">MAPI フォームの必要なインターフェイスと同様、特定のフォームのサーバーが必要なすべての省略可能なインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="e9492-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="e9492-115">詳細については、[フォーム サーバー コードの記述](writing-form-server-code.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9492-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="e9492-116">フォームを使用フォームのオブジェクトとプロパティを持つユーザーの相互作用を処理するためにユーザー インターフェイスのコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="e9492-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="e9492-117">フォームのフォーム構成ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="e9492-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="e9492-118">詳細については、[フォーム構成ファイルの形式のファイル](file-format-of-form-configuration-files.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9492-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="e9492-119">フォームをユーザーのコンピューターにインストールします。</span><span class="sxs-lookup"><span data-stu-id="e9492-119">Installing the form on users' computers.</span></span> <span data-ttu-id="e9492-120">詳細については、[ライブラリにフォームをインストールする](installing-a-form-into-a-library.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9492-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="e9492-121">手順 1 ~ 5 はほとんどの場合、シーケンスで実行するのではなく、同時にします。</span><span class="sxs-lookup"><span data-stu-id="e9492-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="e9492-122">多くのプログラミング プロジェクトと同様に、フォームのサーバーの開発プロセスは、いずれかのでは、特に明確に定義されたシーケンスではありません。</span><span class="sxs-lookup"><span data-stu-id="e9492-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="e9492-123">たとえば、フォーム構成ファイルを作成するのようと、最後に 2 番目のステップですが、段階的に、フォーム構成ファイルを作成するが可能性があります、フォームのサーバーに機能を追加するときに詳細になります。</span><span class="sxs-lookup"><span data-stu-id="e9492-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e9492-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9492-124">See also</span></span>



[<span data-ttu-id="e9492-125">MAPI �̊T�O</span><span class="sxs-lookup"><span data-stu-id="e9492-125">MAPI Concepts</span></span>](mapi-concepts.md)

