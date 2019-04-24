---
title: Round 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: 指定された長さまたは精度で四捨五入されたか切り捨てられた数値を返します。
ms.openlocfilehash: 0afab8c3434aef58c4bb25aee22eefd95732797b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307960"
---
# <a name="round-function-access-custom-web-app"></a><span data-ttu-id="48d4d-103">Round 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="48d4d-103">Round Function (Access custom web app)</span></span>

<span data-ttu-id="48d4d-104">指定された長さまたは精度で四捨五入されたか切り捨てられた数値を返します。</span><span class="sxs-lookup"><span data-stu-id="48d4d-104">Returns a numeric value, either rounded or truncated, to the specified length or precision.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="48d4d-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="48d4d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="48d4d-107">構文</span><span class="sxs-lookup"><span data-stu-id="48d4d-107">Syntax</span></span>

 <span data-ttu-id="48d4d-108">**Round**(*数値*、*精度*、[ *TruncateInsteadOfRound* ])</span><span class="sxs-lookup"><span data-stu-id="48d4d-108">**Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ])</span></span> 
  
<span data-ttu-id="48d4d-109">**Round** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="48d4d-109">The **Round** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="48d4d-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="48d4d-110">**Argument name**</span></span>|<span data-ttu-id="48d4d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="48d4d-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="48d4d-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="48d4d-112">*Number*</span></span>  <br/> |<span data-ttu-id="48d4d-113">数式。</span><span class="sxs-lookup"><span data-stu-id="48d4d-113">A numeric expression.</span></span>  <br/> |
| <span data-ttu-id="48d4d-114">*精度*</span><span class="sxs-lookup"><span data-stu-id="48d4d-114">*Precision*</span></span>  <br/> |<span data-ttu-id="48d4d-115">丸められる桁数\*\* を指定します。</span><span class="sxs-lookup"><span data-stu-id="48d4d-115">The precision to which  *Number*  is to be rounded.</span></span>  <span data-ttu-id="48d4d-116">*精度*は、数値式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="48d4d-116">*Precision*  must be a numeric expression.</span></span> <span data-ttu-id="48d4d-117">*精度*に正の数値を指定すると、引数*number*は引数 length で指定した小数点の桁数に四捨五入されます。</span><span class="sxs-lookup"><span data-stu-id="48d4d-117">When  *Precision*  is a positive number,  *Number*  is rounded to the number of decimal positions specified by length.</span></span> <span data-ttu-id="48d4d-118">*精度*に負の数値を指定すると、引数 length で指定した*数値*が小数点の左側で四捨五入されます。</span><span class="sxs-lookup"><span data-stu-id="48d4d-118">When  *Precision*  is a negative number,  *Number*  is rounded on the left side of the decimal point, as specified by length.</span></span>  <br/> |
| <span data-ttu-id="48d4d-119">*TruncateInsteadOfRound*</span><span class="sxs-lookup"><span data-stu-id="48d4d-119">*TruncateInsteadOfRound*</span></span>  <br/> |<span data-ttu-id="48d4d-120">実行する操作の種類。</span><span class="sxs-lookup"><span data-stu-id="48d4d-120">The type of operation to perform.</span></span> <span data-ttu-id="48d4d-121">省略するか0に設定すると、*数値*は丸められます。</span><span class="sxs-lookup"><span data-stu-id="48d4d-121">When omitted or set to 0,  *Number*  is rounded.</span></span> <span data-ttu-id="48d4d-122">0以外の値を指定すると、*数値*は切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="48d4d-122">When a value other than 0 is specified,  *Number*  is truncated.</span></span> <span data-ttu-id="48d4d-123">既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="48d4d-123">The default value is 0.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48d4d-124">解説</span><span class="sxs-lookup"><span data-stu-id="48d4d-124">Remarks</span></span>

 <span data-ttu-id="48d4d-p104">**Round** は常に値を返します。長さが負の値であり、少数点よりも前の桁数よりも大きい場合、 **Round** は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="48d4d-p104">**Round** always returns a value. If length is negative and larger than the number of digits before the decimal point, **Round** returns 0.</span></span> 
  

