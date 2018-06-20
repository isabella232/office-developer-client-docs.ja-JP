---
title: 一時アドレス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 598ced18d659fcbe52ded07cc3bb80dc396eddbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801691"
---
# <a name="one-off-addresses"></a><span data-ttu-id="2a311-103">一時アドレス</span><span class="sxs-lookup"><span data-stu-id="2a311-103">One-off addresses</span></span>

<span data-ttu-id="2a311-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2a311-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2a311-105">1 回限りのアドレスを使用して、セッションのアドレス帳コンテナーのいずれかに対応するエントリを持たない受信者の一時受信者にメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="2a311-105">One-off addresses are used to send messages to one-off recipients, recipients that do not have a corresponding entry in any of the session's address book containers.</span></span> <span data-ttu-id="2a311-106">クライアントは、アドレス帳または新しい受信者が送信するメッセージの受信者の一覧に新しいエントリを追加するとき、一時アドレスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2a311-106">Clients can create one-off addresses when they add new entries to the address book or new recipients to the recipient list of an outgoing message.</span></span> <span data-ttu-id="2a311-107">一時アドレスは、変更可能なすべてのコンテナーに追加できます。</span><span class="sxs-lookup"><span data-stu-id="2a311-107">One-off addresses can be added to any container that is modifiable.</span></span>
  
<span data-ttu-id="2a311-108">一時アドレスを作成するには、クライアントは、すべての一時アドレスを構成する情報を入力するためのエディット コントロールを含む特別なテンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="2a311-108">To create a one-off address, clients use a special template containing edit controls for entering all of the information that makes up a one-off address.</span></span> <span data-ttu-id="2a311-109">他の種類のアドレスのように、一時アドレスは、定義済みの書式を使用します。</span><span class="sxs-lookup"><span data-stu-id="2a311-109">One-off addresses, like addresses of other types, use a predefined format.</span></span> <span data-ttu-id="2a311-110">一時アドレスの形式は、MAPI によって次のように定義されます。</span><span class="sxs-lookup"><span data-stu-id="2a311-110">The one-off address format is defined by MAPI as follows:</span></span>
  
`Display name[Address type:Email address]`
  
<span data-ttu-id="2a311-111">6 つのコンポーネントをこの形式と文字の引用のいくつかのルールがあります。</span><span class="sxs-lookup"><span data-stu-id="2a311-111">There are six components to this format and some rules about quoting characters.</span></span> <span data-ttu-id="2a311-112">コンポーネントは、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="2a311-112">The components are described in the following table.</span></span>
  
|<span data-ttu-id="2a311-113">**コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="2a311-113">**Component**</span></span>|<span data-ttu-id="2a311-114">**使用例**</span><span class="sxs-lookup"><span data-stu-id="2a311-114">**Usage**</span></span>|<span data-ttu-id="2a311-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="2a311-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2a311-116">表示名</span><span class="sxs-lookup"><span data-stu-id="2a311-116">Display name</span></span>  <br/> |<span data-ttu-id="2a311-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="2a311-117">Optional</span></span>  <br/> |<span data-ttu-id="2a311-118">存在しない場合、 **IAddrBook::ResolveName**は、表示名として電子メール アドレスの表示部分を使用します。</span><span class="sxs-lookup"><span data-stu-id="2a311-118">If not present, **IAddrBook::ResolveName** uses the visible part of the email address as the display name.</span></span> <span data-ttu-id="2a311-119">空白を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2a311-119">May include blanks.</span></span> <span data-ttu-id="2a311-120">詳細については、 [IAddrBook::ResolveName](iaddrbook-resolvename.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a311-120">For more information, see [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>  <br/> |
|<span data-ttu-id="2a311-121">[</span><span class="sxs-lookup"><span data-stu-id="2a311-121"></span></span>  <br/> |<span data-ttu-id="2a311-122">必須</span><span class="sxs-lookup"><span data-stu-id="2a311-122">Required</span></span>  <br/> |<span data-ttu-id="2a311-123">種類とアドレス情報の始まりのようになります。</span><span class="sxs-lookup"><span data-stu-id="2a311-123">Delineates the start of the type and address information.</span></span>  <br/> |
|<span data-ttu-id="2a311-124">]</span><span class="sxs-lookup"><span data-stu-id="2a311-124"></span></span>  <br/> |<span data-ttu-id="2a311-125">必須</span><span class="sxs-lookup"><span data-stu-id="2a311-125">Required</span></span>  <br/> |<span data-ttu-id="2a311-126">タイプとアドレスの情報の最後のようになります。</span><span class="sxs-lookup"><span data-stu-id="2a311-126">Delineates the end of the type and address information.</span></span> <span data-ttu-id="2a311-127">この文字を次の空白以外の値エントリは、カスタム受信者として見なされません。</span><span class="sxs-lookup"><span data-stu-id="2a311-127">If anything other than white space follows this character, the entry is not treated as a custom recipient.</span></span>  <br/> |
|<span data-ttu-id="2a311-128">アドレスの種類</span><span class="sxs-lookup"><span data-stu-id="2a311-128">Address type</span></span>  <br/> |<span data-ttu-id="2a311-129">必須</span><span class="sxs-lookup"><span data-stu-id="2a311-129">Required</span></span>  <br/> |<span data-ttu-id="2a311-130">アドレスの種類特定のアドレスの形式にマップします。</span><span class="sxs-lookup"><span data-stu-id="2a311-130">Type of address; maps to a specific address format.</span></span> <span data-ttu-id="2a311-131">詳細については、 [MAPI のアドレスの種類](mapi-address-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a311-131">For more information, see [MAPI Address Types](mapi-address-types.md).</span></span>  <br/> |
|<span data-ttu-id="2a311-132">:</span><span class="sxs-lookup"><span data-stu-id="2a311-132"></span></span>  <br/> |<span data-ttu-id="2a311-133">必須</span><span class="sxs-lookup"><span data-stu-id="2a311-133">Required</span></span>  <br/> |<span data-ttu-id="2a311-134">電子メール アドレスからアドレスの種類を区切ります。</span><span class="sxs-lookup"><span data-stu-id="2a311-134">Separates the address type from the email address.</span></span>  <br/> |
|<span data-ttu-id="2a311-135">メール アドレス</span><span class="sxs-lookup"><span data-stu-id="2a311-135">Email address</span></span>  <br/> |<span data-ttu-id="2a311-136">必須</span><span class="sxs-lookup"><span data-stu-id="2a311-136">Required</span></span>  <br/> |<span data-ttu-id="2a311-137">��M�҂̃A�h���X�ł��B</span><span class="sxs-lookup"><span data-stu-id="2a311-137">Address of the recipient.</span></span> <span data-ttu-id="2a311-138">空白を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2a311-138">May include blanks.</span></span>  <br/> |
   
<span data-ttu-id="2a311-139">MAPI では、文字を引用符で囲むの特定のセットを使用して、左角かっこ ()、カンマ (,) などの特殊文字を格納するためのアドレスを許可して、コロン (:) と、改行などのいくつかの untypeable 文字を返したり、フィードやその他の任意の 16 進表現の行です。</span><span class="sxs-lookup"><span data-stu-id="2a311-139">MAPI uses particular sets of quoting characters to allow addresses to contain special characters such as comma (,), left bracket ([), and colon (:) and some untypeable characters such as the carriage return or line feed or any other hexadecimal equivalent.</span></span> <span data-ttu-id="2a311-140">引用符文字は、円記号 (\)。</span><span class="sxs-lookup"><span data-stu-id="2a311-140">The quoting character is the backslash (\).</span></span> <span data-ttu-id="2a311-141">したがって、クライアントやプロバイダーは、アドレスで、円記号を挿入する必要がある場合に、する必要があります撤廃クォート文字を持つこと ("\\")。</span><span class="sxs-lookup"><span data-stu-id="2a311-141">Therefore, if clients or providers must insert a backslash in an address, they must preceed it with the quoting character ("\\").</span></span>
  
<span data-ttu-id="2a311-142">クライアントとサービス ・ プロバイダーの場合は]、印字可能なフィールドのいずれかでこの見積りの手法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a311-142">Clients and service providers can use this quoting technique in any of the nonfixed, typeable fields.</span></span> <span data-ttu-id="2a311-143">次のエントリが表示名、アドレスの種類として MSPEER と Lee を部品に変換するなどと\\e メール アドレスとして billll\in。</span><span class="sxs-lookup"><span data-stu-id="2a311-143">For example, the following entry translates to Bill Lee as the display name, MSPEER as the address type, and \\billll\in as the email address:</span></span>
  
`Bill Lee[MSPEER:\\\\billl\in]`

<span data-ttu-id="2a311-144">Nontypeable の特殊文字を挿入するには、クライアントとサービス ・ プロバイダーは、対応する 16 進数を表す x と 2 つの 16 進数の後に、引用符文字を使用します。</span><span class="sxs-lookup"><span data-stu-id="2a311-144">To insert special nontypeable characters, clients and service providers use a quoting character followed by an x and two hexadecimal digits to represent their hexadecimal equivalent.</span></span> <span data-ttu-id="2a311-145">たとえば、アドレスは改行文字に相当する nontypeable 文字を含む場合は、戻るには、(\0d) の 16 進数、クライアントは入力として。</span><span class="sxs-lookup"><span data-stu-id="2a311-145">For example, if an address has a nontypeable character that equates to a carriage return, (\0d) in hexadecimal, a client would enter them as:</span></span>
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

<span data-ttu-id="2a311-146">**IAddrBook::ResolveName**には、次の形式のアドレスを探して、ほとんどの SMTP アドレスも自動的に解析します。</span><span class="sxs-lookup"><span data-stu-id="2a311-146">**IAddrBook::ResolveName** also automatically parses most SMTP addresses, looking for addresses with the following format:</span></span> 
  
`XXX@YYY.ZZZ`

<span data-ttu-id="2a311-147">RFC822 形式のすべてを処理すると、この自動解析がほとんどのユーザーのための適切です。</span><span class="sxs-lookup"><span data-stu-id="2a311-147">Although not all of the possible RFC822 formats are handled, this automatic parsing is adequate for most users.</span></span> <span data-ttu-id="2a311-148">**ResolveName**には、ユーザーがメッセージに直接 SMTP アドレスを入力し、インターネット ユーザーにメッセージを有効にするには、この機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2a311-148">**ResolveName** includes this functionality to enable users to enter SMTP addresses directly into a message and have that message go to the Internet user.</span></span> <span data-ttu-id="2a311-149">アドレスの XXX、YYY、ZZZ の各要素には、1 つまたは複数の文字を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a311-149">The XXX, YYY, and ZZZ components of the address can be one or more characters.</span></span> <span data-ttu-id="2a311-150">アットマーク (@) に含まれてすることはできません XXX、YYY、または ZZZ のいずれかのアドレスのコンポーネントと、YYY コンポーネントも含めることはできません期間。</span><span class="sxs-lookup"><span data-stu-id="2a311-150">The at sign (@) cannot be included in either the XXX, YYY, or ZZZ address components and the YYY component also cannot include the period.</span></span> <span data-ttu-id="2a311-151">次の文字は SMTP アドレス内の特殊文字であるため、MAPI が自動的に 1 回限りのアドレスにこれらの文字を含む表示名に変換されます。</span><span class="sxs-lookup"><span data-stu-id="2a311-151">Because the following characters are special characters in SMTP addresses, MAPI automatically converts a display name containing these characters into a one-off address:</span></span> 
  
- \>\>
    
- @
    
- \<\>
    
- <span data-ttu-id="2a311-152">.</span><span class="sxs-lookup"><span data-stu-id="2a311-152"></span></span>
    
<span data-ttu-id="2a311-153">各 1 回限りのアドレスには、対応する一時エントリ id が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2a311-153">Every one-off address is assigned a corresponding one-off entry identifier.</span></span> <span data-ttu-id="2a311-154">この割り当てをするためには、クライアントが**IAddrBook::CreateOneOff**を呼び出すし、トランスポート プロバイダーは、 **IMAPISupport::CreateOneOff**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2a311-154">To make this assignment, clients call **IAddrBook::CreateOneOff** and transport providers call **IMAPISupport::CreateOneOff**.</span></span> <span data-ttu-id="2a311-155">詳細については、 [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)および[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a311-155">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) and [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).</span></span> <span data-ttu-id="2a311-156">受信メッセージを処理するには、トランスポート プロバイダーは、ゲートウェイ アドレスとトランスポートの関連付けられているアドレス帳プロバイダーによっては処理できないアドレスの 1 回限りのエントリの識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="2a311-156">When processing incoming messages, transport providers create one-off entry identifiers for gateway addresses and for addresses that cannot be handled by the transport's associated address book providers.</span></span> <span data-ttu-id="2a311-157">トランスポート プロバイダーは、メッセージ トランスポートに関連付けられているアドレス帳プロバイダーによって処理できるかどうかを決定するには、各アドレスの種類を確認します。</span><span class="sxs-lookup"><span data-stu-id="2a311-157">Transport providers check the type of each address in a message to determine if it can be handled by an address book provider associated with the transport.</span></span> <span data-ttu-id="2a311-158">できない場合は、トランスポート プロバイダーは、1 回限りのエントリの識別子を使用してアドレスを関連付けるには**IMAPISupport::CreateOneOff**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2a311-158">If it cannot, transport providers call **IMAPISupport::CreateOneOff** to associate the address with a one-off entry identifier.</span></span> 
  
<span data-ttu-id="2a311-159">一時エントリ id には、次の順序で次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2a311-159">One-off entry identifiers include the following information in the following order:</span></span>
  
1. <span data-ttu-id="2a311-160">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="2a311-160">**MAPIUID**</span></span>
    
2. <span data-ttu-id="2a311-161">バージョン</span><span class="sxs-lookup"><span data-stu-id="2a311-161">Version</span></span>
    
3. <span data-ttu-id="2a311-162">フラグ</span><span class="sxs-lookup"><span data-stu-id="2a311-162">Flags</span></span>
    
4. <span data-ttu-id="2a311-163">表示名</span><span class="sxs-lookup"><span data-stu-id="2a311-163">Display name</span></span>
    
5. <span data-ttu-id="2a311-164">アドレスの種類</span><span class="sxs-lookup"><span data-stu-id="2a311-164">Address type</span></span>
    
6. <span data-ttu-id="2a311-165">メール アドレス</span><span class="sxs-lookup"><span data-stu-id="2a311-165">Email address</span></span>
    
<span data-ttu-id="2a311-166">**IAddrBook::CreateOneOff**および**IMAPISupport::CreateOneOff**への呼び出し、クライアントおよびトランスポート プロバイダーを設定できます 1 回限りのアドレスで表される受信者が書式設定されたテキストを処理できるかどうかまたは OLE の埋め込みを示すフラグオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="2a311-166">In the calls to **IAddrBook::CreateOneOff** and **IMAPISupport::CreateOneOff**, clients and transport providers can set a flag that indicates whether or not the recipient represented by the one-off address can process formatted text or embedded OLE objects.</span></span> <span data-ttu-id="2a311-167">受信者が書式付きテキスト、およびクライアントと、 _ulFlags_パラメーターに MAPI_SEND_NO_RICH_INFO フラグを設定しますトランスポート プロバイダーは、OLE オブジェクトを処理できることを示します。</span><span class="sxs-lookup"><span data-stu-id="2a311-167">To indicate that a recipient can handle formatted text and OLE objects, clients and transport providers set the MAPI_SEND_NO_RICH_INFO flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="2a311-168">MAPI は、1 回限りの受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) のプロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="2a311-168">MAPI then sets the one-off recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="2a311-169">このフラグが設定されていない、MAPI は 1 回限りのアドレスが SMTP アドレスとして解釈される場合を除き、true を指定する**PR_SEND_RICH_INFO**を設定します。</span><span class="sxs-lookup"><span data-stu-id="2a311-169">When this flag is not set, MAPI sets **PR_SEND_RICH_INFO** to TRUE unless the one-off address is interpreted as an SMTP address.</span></span> <span data-ttu-id="2a311-170">この 1 つの場合では、 **PR_SEND_RICH_INFO**デフォルト値は FALSE です。</span><span class="sxs-lookup"><span data-stu-id="2a311-170">In this one case, **PR_SEND_RICH_INFO** defaults to FALSE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2a311-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a311-171">See also</span></span>

- [<span data-ttu-id="2a311-172">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="2a311-172">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)

