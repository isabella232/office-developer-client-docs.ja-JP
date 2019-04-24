---
title: 一時アドレス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e6bda55951d8df5c5da272750c631ec105b2ccf2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279637"
---
# <a name="one-off-addresses"></a><span data-ttu-id="3c811-103">一時アドレス</span><span class="sxs-lookup"><span data-stu-id="3c811-103">One-off addresses</span></span>

<span data-ttu-id="3c811-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c811-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c811-105">一時アドレスは、1回限りの受信者にメッセージを送信するために使用されます。受信者は、セッションのアドレス帳コンテナーのいずれかに対応するエントリがないことになります。</span><span class="sxs-lookup"><span data-stu-id="3c811-105">One-off addresses are used to send messages to one-off recipients, recipients that do not have a corresponding entry in any of the session's address book containers.</span></span> <span data-ttu-id="3c811-106">クライアントは、送信メッセージの受信者一覧に新しいエントリをアドレス帳または新しい受信者に追加するときに、1回限りのアドレスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="3c811-106">Clients can create one-off addresses when they add new entries to the address book or new recipients to the recipient list of an outgoing message.</span></span> <span data-ttu-id="3c811-107">変更可能な任意のコンテナーに、1回限りのアドレスを追加できます。</span><span class="sxs-lookup"><span data-stu-id="3c811-107">One-off addresses can be added to any container that is modifiable.</span></span>
  
<span data-ttu-id="3c811-108">1回限りのアドレスを作成するには、クライアントは編集コントロールを含む特別なテンプレートを使用して、1回限りのアドレスを構成するすべての情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="3c811-108">To create a one-off address, clients use a special template containing edit controls for entering all of the information that makes up a one-off address.</span></span> <span data-ttu-id="3c811-109">その他の種類のアドレスなどの1回限りのアドレスは、定義済みの形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="3c811-109">One-off addresses, like addresses of other types, use a predefined format.</span></span> <span data-ttu-id="3c811-110">1回限りのアドレス形式は、次のように MAPI によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="3c811-110">The one-off address format is defined by MAPI as follows:</span></span>
  
`Display name[Address type:Email address]`
  
<span data-ttu-id="3c811-111">この形式には6つのコンポーネントがあり、文字のクォートにはいくつかのルールがあります。</span><span class="sxs-lookup"><span data-stu-id="3c811-111">There are six components to this format and some rules about quoting characters.</span></span> <span data-ttu-id="3c811-112">次の表では、これらのコンポーネントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3c811-112">The components are described in the following table.</span></span>
  
|<span data-ttu-id="3c811-113">**コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="3c811-113">**Component**</span></span>|<span data-ttu-id="3c811-114">**用途**</span><span class="sxs-lookup"><span data-stu-id="3c811-114">**Usage**</span></span>|<span data-ttu-id="3c811-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="3c811-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3c811-116">識別名 (DN)</span><span class="sxs-lookup"><span data-stu-id="3c811-116">Display name</span></span>  <br/> |<span data-ttu-id="3c811-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="3c811-117">Optional</span></span>  <br/> |<span data-ttu-id="3c811-118">存在しない場合、 **IAddrBook:: ResolveName**は、電子メールアドレスの表示名として表示される部分を使用します。</span><span class="sxs-lookup"><span data-stu-id="3c811-118">If not present, **IAddrBook::ResolveName** uses the visible part of the email address as the display name.</span></span> <span data-ttu-id="3c811-119">空白を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3c811-119">May include blanks.</span></span> <span data-ttu-id="3c811-120">詳細については、「 [IAddrBook:: ResolveName](iaddrbook-resolvename.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c811-120">For more information, see [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>  <br/> |
|<span data-ttu-id="3c811-121">[</span><span class="sxs-lookup"><span data-stu-id="3c811-121"></span></span>  <br/> |<span data-ttu-id="3c811-122">必須</span><span class="sxs-lookup"><span data-stu-id="3c811-122">Required</span></span>  <br/> |<span data-ttu-id="3c811-123">表しの種類と住所情報の開始。</span><span class="sxs-lookup"><span data-stu-id="3c811-123">Delineates the start of the type and address information.</span></span>  <br/> |
|<span data-ttu-id="3c811-124">]</span><span class="sxs-lookup"><span data-stu-id="3c811-124"></span></span>  <br/> |<span data-ttu-id="3c811-125">必須</span><span class="sxs-lookup"><span data-stu-id="3c811-125">Required</span></span>  <br/> |<span data-ttu-id="3c811-126">表しは、型と住所情報の最後を示します。</span><span class="sxs-lookup"><span data-stu-id="3c811-126">Delineates the end of the type and address information.</span></span> <span data-ttu-id="3c811-127">この文字の後に空白以外の文字を入力した場合、エントリはカスタム受信者として扱われません。</span><span class="sxs-lookup"><span data-stu-id="3c811-127">If anything other than white space follows this character, the entry is not treated as a custom recipient.</span></span>  <br/> |
|<span data-ttu-id="3c811-128">アドレスの種類</span><span class="sxs-lookup"><span data-stu-id="3c811-128">Address type</span></span>  <br/> |<span data-ttu-id="3c811-129">必須</span><span class="sxs-lookup"><span data-stu-id="3c811-129">Required</span></span>  <br/> |<span data-ttu-id="3c811-130">住所の種類。特定のアドレス形式にマップします。</span><span class="sxs-lookup"><span data-stu-id="3c811-130">Type of address; maps to a specific address format.</span></span> <span data-ttu-id="3c811-131">詳細については、「 [MAPI アドレスの種類](mapi-address-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c811-131">For more information, see [MAPI Address Types](mapi-address-types.md).</span></span>  <br/> |
|<span data-ttu-id="3c811-132">:</span><span class="sxs-lookup"><span data-stu-id="3c811-132"></span></span>  <br/> |<span data-ttu-id="3c811-133">必須</span><span class="sxs-lookup"><span data-stu-id="3c811-133">Required</span></span>  <br/> |<span data-ttu-id="3c811-134">アドレスの種類を電子メールアドレスから分離します。</span><span class="sxs-lookup"><span data-stu-id="3c811-134">Separates the address type from the email address.</span></span>  <br/> |
|<span data-ttu-id="3c811-135">電子メール アドレス</span><span class="sxs-lookup"><span data-stu-id="3c811-135">Email address</span></span>  <br/> |<span data-ttu-id="3c811-136">必須</span><span class="sxs-lookup"><span data-stu-id="3c811-136">Required</span></span>  <br/> |<span data-ttu-id="3c811-137">��M�҂̃A�h���X�ł��B</span><span class="sxs-lookup"><span data-stu-id="3c811-137">Address of the recipient.</span></span> <span data-ttu-id="3c811-138">空白を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3c811-138">May include blanks.</span></span>  <br/> |
   
<span data-ttu-id="3c811-139">MAPI では、特定の引用符文字のセットを使用して、コンマ (,)、左大かっこ ([)、コロン (:) などの特殊文字をアドレスに含めることができます。また、キャリッジリターンや改行などの何らかのシリアライズ可能な文字、またはその他の16進数に相当するものもあります。</span><span class="sxs-lookup"><span data-stu-id="3c811-139">MAPI uses particular sets of quoting characters to allow addresses to contain special characters such as comma (,), left bracket ([), and colon (:) and some untypeable characters such as the carriage return or line feed or any other hexadecimal equivalent.</span></span> <span data-ttu-id="3c811-140">クォート文字は、バックスラッシュ (\)) です。</span><span class="sxs-lookup"><span data-stu-id="3c811-140">The quoting character is the backslash (\).</span></span> <span data-ttu-id="3c811-141">そのため、クライアントまたはプロバイダーがアドレスにバックスラッシュを挿入する必要がある場合は、その preceed を\\クォート文字 ("") で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c811-141">Therefore, if clients or providers must insert a backslash in an address, they must preceed it with the quoting character ("\\").</span></span>
  
<span data-ttu-id="3c811-142">クライアントおよびサービスプロバイダーは、固定されていない任意の型のフィールドでこのクォート手法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3c811-142">Clients and service providers can use this quoting technique in any of the nonfixed, typeable fields.</span></span> <span data-ttu-id="3c811-143">たとえば、次のエントリは、請求書 Lee を表示名、アドレスの種類\\としては mルード、電子メールアドレスとしては、次のように変換します。</span><span class="sxs-lookup"><span data-stu-id="3c811-143">For example, the following entry translates to Bill Lee as the display name, MSPEER as the address type, and \\billll\in as the email address:</span></span>
  
`Bill Lee[MSPEER:\\\\billl\in]`

<span data-ttu-id="3c811-144">特別な非種類のシリアライズ可能な文字を挿入するには、クライアントとサービスプロバイダーは、クォート文字の後に x と2桁の16進数を使用して、それに相当する16進数を表します。</span><span class="sxs-lookup"><span data-stu-id="3c811-144">To insert special nontypeable characters, clients and service providers use a quoting character followed by an x and two hexadecimal digits to represent their hexadecimal equivalent.</span></span> <span data-ttu-id="3c811-145">たとえば、アドレスに、キャリッジリターンに相当する非検出可能な文字 (\ 0d) がある場合、16進数ではクライアントは次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="3c811-145">For example, if an address has a nontypeable character that equates to a carriage return, (\0d) in hexadecimal, a client would enter them as:</span></span>
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

<span data-ttu-id="3c811-146">**IAddrBook:: ResolveName**は、ほとんどの SMTP アドレスを自動的に解析し、次の形式のアドレスを検索します。</span><span class="sxs-lookup"><span data-stu-id="3c811-146">**IAddrBook::ResolveName** also automatically parses most SMTP addresses, looking for addresses with the following format:</span></span> 
  
`XXX@YYY.ZZZ`

<span data-ttu-id="3c811-147">使用可能な RFC822 形式の一部は処理されませんが、ほとんどのユーザーにとってこの自動解析は十分です。</span><span class="sxs-lookup"><span data-stu-id="3c811-147">Although not all of the possible RFC822 formats are handled, this automatic parsing is adequate for most users.</span></span> <span data-ttu-id="3c811-148">**ResolveName**にはこの機能が含まれており、ユーザーが SMTP アドレスを直接メッセージに入力し、そのメッセージがインターネットユーザーに送られるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="3c811-148">**ResolveName** includes this functionality to enable users to enter SMTP addresses directly into a message and have that message go to the Internet user.</span></span> <span data-ttu-id="3c811-149">住所の XXX、YYY、および ZZZ コンポーネントには、1つ以上の文字を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3c811-149">The XXX, YYY, and ZZZ components of the address can be one or more characters.</span></span> <span data-ttu-id="3c811-150">アットマーク (@) は、XXX、yyy、または ZZZ のいずれかのアドレスコンポーネントに含めることはできません。また、yyy コンポーネントに期間を含めることもできません。</span><span class="sxs-lookup"><span data-stu-id="3c811-150">The at sign (@) cannot be included in either the XXX, YYY, or ZZZ address components and the YYY component also cannot include the period.</span></span> <span data-ttu-id="3c811-151">SMTP アドレスでは次の文字が特殊文字なので、MAPI はこれらの文字を含む表示名を、1回限りのアドレスに自動的に変換します。</span><span class="sxs-lookup"><span data-stu-id="3c811-151">Because the following characters are special characters in SMTP addresses, MAPI automatically converts a display name containing these characters into a one-off address:</span></span> 
  
- \>\>
    
- @
    
- \<\>
    
- <span data-ttu-id="3c811-152">.</span><span class="sxs-lookup"><span data-stu-id="3c811-152"></span></span>
    
<span data-ttu-id="3c811-153">すべての1回限りのアドレスには、対応する1回限りのエントリ識別子が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="3c811-153">Every one-off address is assigned a corresponding one-off entry identifier.</span></span> <span data-ttu-id="3c811-154">この割り当てを行うために、クライアントは**IAddrBook:: createoneoff**を呼び出し、トランスポートプロバイダは**imapisupport:: createoneoff**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3c811-154">To make this assignment, clients call **IAddrBook::CreateOneOff** and transport providers call **IMAPISupport::CreateOneOff**.</span></span> <span data-ttu-id="3c811-155">詳細については、「 [IAddrBook:: createoneoff](iaddrbook-createoneoff.md) 」および「 [imapisupport:: createoneoff](imapisupport-createoneoff.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c811-155">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) and [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).</span></span> <span data-ttu-id="3c811-156">受信メッセージを処理する場合、トランスポートプロバイダーは、ゲートウェイアドレスと、トランスポートに関連付けられたアドレス帳プロバイダーによって処理できないアドレスに対して、1回限りのエントリ識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="3c811-156">When processing incoming messages, transport providers create one-off entry identifiers for gateway addresses and for addresses that cannot be handled by the transport's associated address book providers.</span></span> <span data-ttu-id="3c811-157">トランスポートプロバイダーメッセージ内の各アドレスの種類をチェックして、トランスポートに関連付けられているアドレス帳プロバイダーによって処理できるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="3c811-157">Transport providers check the type of each address in a message to determine if it can be handled by an address book provider associated with the transport.</span></span> <span data-ttu-id="3c811-158">送信できない場合、トランスポートプロバイダーは**imapisupport:: createoneoff**を呼び出して、アドレスを1回限りのエントリ識別子に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="3c811-158">If it cannot, transport providers call **IMAPISupport::CreateOneOff** to associate the address with a one-off entry identifier.</span></span> 
  
<span data-ttu-id="3c811-159">1回限りのエントリ識別子には、次の順序で情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3c811-159">One-off entry identifiers include the following information in the following order:</span></span>
  
1. <span data-ttu-id="3c811-160">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="3c811-160">**MAPIUID**</span></span>
    
2. <span data-ttu-id="3c811-161">バージョン</span><span class="sxs-lookup"><span data-stu-id="3c811-161">Version</span></span>
    
3. <span data-ttu-id="3c811-162">フラグ</span><span class="sxs-lookup"><span data-stu-id="3c811-162">Flags</span></span>
    
4. <span data-ttu-id="3c811-163">識別名 (DN)</span><span class="sxs-lookup"><span data-stu-id="3c811-163">Display name</span></span>
    
5. <span data-ttu-id="3c811-164">アドレスの種類</span><span class="sxs-lookup"><span data-stu-id="3c811-164">Address type</span></span>
    
6. <span data-ttu-id="3c811-165">電子メール アドレス</span><span class="sxs-lookup"><span data-stu-id="3c811-165">Email address</span></span>
    
<span data-ttu-id="3c811-166">**IAddrBook:: createoneoff**および**imapisupport:: createoneoff**の場合、クライアントとトランスポートプロバイダーは、1回限りのアドレスで表される受信者が書式設定されたテキストや埋め込み OLE を処理できるかどうかを示すフラグを設定できます。対象.</span><span class="sxs-lookup"><span data-stu-id="3c811-166">In the calls to **IAddrBook::CreateOneOff** and **IMAPISupport::CreateOneOff**, clients and transport providers can set a flag that indicates whether or not the recipient represented by the one-off address can process formatted text or embedded OLE objects.</span></span> <span data-ttu-id="3c811-167">受信者が書式設定されたテキストと OLE オブジェクトを処理できることを示すために、クライアントとトランスポートプロバイダーは_ulflags_パラメーターに MAPI_SEND_NO_RICH_INFO フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="3c811-167">To indicate that a recipient can handle formatted text and OLE objects, clients and transport providers set the MAPI_SEND_NO_RICH_INFO flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="3c811-168">その後、MAPI は、1回限りの受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="3c811-168">MAPI then sets the one-off recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="3c811-169">このフラグが設定されていない場合、MAPI は、1回限りのアドレスが SMTP アドレスとして解釈される場合を除き、 **PR_SEND_RICH_INFO**を TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="3c811-169">When this flag is not set, MAPI sets **PR_SEND_RICH_INFO** to TRUE unless the one-off address is interpreted as an SMTP address.</span></span> <span data-ttu-id="3c811-170">この1つの場合、 **PR_SEND_RICH_INFO**の既定値は FALSE です。</span><span class="sxs-lookup"><span data-stu-id="3c811-170">In this one case, **PR_SEND_RICH_INFO** defaults to FALSE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c811-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c811-171">See also</span></span>

- [<span data-ttu-id="3c811-172">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="3c811-172">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)

