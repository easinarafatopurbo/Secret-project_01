<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Fecedook — Share Your Secret</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="min-h-screen bg-gradient-to-r from-indigo-100 to-purple-100 flex items-center justify-center p-6">
  <div class="w-full max-w-lg bg-white rounded-2xl shadow-2xl p-8">
    <h1 class="text-3xl font-extrabold text-center text-indigo-600 mb-2">Fecedook</h1>
    <p class="text-center text-slate-600 mb-6">Share a fun little secret — safely and anonymously!</p>

    <form action="https://formspree.io/f/xrblnwnr" method="POST" class="space-y-5">
      <!-- Nickname -->
      <div>
        <label for="nickname" class="block font-semibold text-slate-800">Nickname (optional)</label>
        <input id="nickname" name="nickname" type="text" maxlength="40"
          class="mt-2 w-full rounded-xl border border-slate-200 focus:border-indigo-400 focus:ring-2 focus:ring-indigo-200 p-3 placeholder-slate-400"
          placeholder="Leave blank if you want to stay anonymous" />
      </div>

      <!-- Phone (optional) -->
      <div>
        <label for="phone" class="block font-semibold text-slate-800">Phone number (optional)</label>
        <input id="phone" name="phone" type="tel" pattern="[0-9+\-\\s]{6,20}"
          class="mt-2 w-full rounded-xl border border-slate-200 focus:border-indigo-400 focus:ring-2 focus:ring-indigo-200 p-3 placeholder-slate-400"
          placeholder="Only if you want to share it" />
        <p class="text-xs text-slate-500 mt-1">Never share account passwords or OTPs here.</p>
      </div>

      <!-- Shared code -->
      <div>
        <label for="shared_code" class="block font-semibold text-slate-800">Shared code (optional)</label>
        <input id="shared_code" name="shared_code" type="text" maxlength="20"
          class="mt-2 w-full rounded-xl border border-slate-200 focus:border-indigo-400 focus:ring-2 focus:ring-indigo-200 p-3 placeholder-slate-400"
          placeholder="Like SUN123, agreed beforehand" />
      </div>

      <!-- Secret message -->
      <div>
        <label for="message" class="block font-semibold text-slate-800">Your secret</label>
        <textarea id="message" name="message" rows="4" required
          class="mt-2 w-full rounded-xl border border-slate-200 focus:border-indigo-400 focus:ring-2 focus:ring-indigo-200 p-3 placeholder-slate-400"
          placeholder="Write your secret here..."></textarea>
      </div>

      <!-- Consent -->
      <div class="flex items-start gap-2 mt-2">
        <input id="consent" name="consent" type="checkbox" required class="mt-1">
        <label for="consent" class="text-sm text-slate-700">I confirm I am sharing this voluntarily and NOT sharing any account password/OTP.</label>
      </div>

      <!-- Submit button -->
      <button type="submit"
        class="w-full py-3 rounded-xl bg-indigo-500 hover:bg-indigo-600 text-white font-semibold shadow-md transition">Submit Secret</button>
    </form>

    <!-- Safety note -->
    <div class="mt-6 text-slate-600 text-sm">
      <p class="font-semibold">Safety First:</p>
      <ul class="list-disc pl-5 space-y-1 mt-1">
        <li>Do not enter any account passwords or OTPs.</li>
        <li>Only share thoughts, fun secrets, or optional contact info.</li>
        <li>Your message will be delivered securely via Formspree.</li>
      </ul>
    </div>
  </div>
</body>
</html>
