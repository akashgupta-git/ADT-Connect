# ADTConnect

**ADTConnect** is a comprehensive video conferencing and digital learning platform designed for MIT ADT University. It unifies secure video calls, meeting management, and academic resource sharing into a single, modern interface. Built with Next.js and TypeScript, it leverages powerful cloud services to ensure reliability and scalability.

## 🚀 Features

  * **🔐 Secure Authentication**: Robust user management (Sign Up/Sign In) powered by **Clerk**, including protection for private routes.
  * **📹 Real-time Video Conferencing**: High-quality audio and video calls using **Stream Video SDK**.
      * **Instant Meetings**: Start a call immediately with a generated link.
      * **Schedule Meetings**: Plan future meetings with date and time selection.
      * **Join via Link**: Easy access to meetings using shared invitation links.
      * **Personal Meeting Room**: A unique, persistent meeting link for every user.
  * **🎥 Meeting Recordings**: Ability to record calls and access/review past meeting recordings later.
  * **📂 Academic Resources**: A centralized file sharing system where users can upload, preview, and download study materials, powered by **Appwrite Storage**.
  * **📱 Responsive Design**: Fully responsive UI built with **Tailwind CSS** and **Shadcn UI**, ensuring a seamless experience across desktop and mobile devices.
  * **🎨 Modern UI/UX**: Features a clean, dark-themed interface with intuitive navigation.

## 🛠️ Tech Stack

**Frontend & Framework:**

  * [Next.js 14+](https://nextjs.org/) (App Router, Server Actions)
  * [TypeScript](https://www.typescriptlang.org/)
  * [React](https://react.dev/)

**Styling & UI:**

  * [Tailwind CSS](https://tailwindcss.com/)
  * [Shadcn UI](https://ui.shadcn.com/)
  * [Lucide React](https://lucide.dev/) (Icons)

**Backend Services & Integrations:**

  * **Authentication**: [Clerk](https://clerk.com/)
  * **Video/Audio**: [GetStream.io](https://getstream.io/video/) (Stream Video React SDK)
  * **Database & Storage**: [Appwrite](https://appwrite.io/)

## ⚙️ Prerequisites

Before you begin, ensure you have the following installed:

  * Node.js (v18 or higher)
  * npm

You will also need accounts and API keys for:

1.  **Clerk** (Authentication)
2.  **Stream** (Video Calling)
3.  **Appwrite** (File Storage)

## 📦 Installation & Setup

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/akashgupta-git/ADT-Connect.git
    cd ADT-Connect
    ```

2.  **Install dependencies:**

    ```bash
    npm install
    ```

3.  **Set up Environment Variables:**
    Create a `.env.local` file in the root directory and add the following keys:

    ```env
    # Clerk Authentication
    NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
    CLERK_SECRET_KEY=your_clerk_secret_key
    NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
    NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up

    # Stream Video
    NEXT_PUBLIC_STREAM_API_KEY=your_stream_api_key
    STREAM_SECRET_KEY=your_stream_secret_key

    # Appwrite (For Resources/File Uploads)
    NEXT_PUBLIC_APPWRITE_ENDPOINT=https://cloud.appwrite.io/v1
    NEXT_PUBLIC_APPWRITE_PROJECT_ID=your_appwrite_project_id
    NEXT_PUBLIC_APPWRITE_BUCKET_ID=your_appwrite_storage_bucket_id

    # Application Base URL
    NEXT_PUBLIC_BASE_URL=http://localhost:3000
    ```

4.  **Run the development server:**

    ```bash
    npm run dev
    ```

5.  **Access the application:**
    Open [http://localhost:3000](https://www.google.com/search?q=http://localhost:3000) in your browser.

## 📂 Project Structure

```bash
├── actions/        # Server actions (e.g., Stream token generation)
├── app/            # Next.js App Router pages
│   ├── (auth)/     # Authentication routes (sign-in, sign-up)
│   ├── (root)/     # Main application routes
│   │   ├── (home)/ # Dashboard, Recordings, Resources, etc.
│   │   └── meeting/[id]/ # Active meeting room page
├── components/     # Reusable UI components
│   ├── ui/         # Shadcn UI primitives
├── constants/      # Static data (sidebar links, avatars)
├── hooks/          # Custom React hooks (useGetCalls, etc.)
├── lib/            # Utility functions and Appwrite client setup
├── providers/      # Context providers (StreamVideoProvider)
└── public/         # Static assets (icons, images)
```

Here is a polished, professional, and license-safe addition you can place at the end of your README:

---

## 🤝 Open for Open-Source Contributions

We welcome and encourage open-source contributions!
Whether you want to fix bugs, improve documentation, add new features, or optimize existing ones — your contributions are appreciated.

### How to Contribute

1. **Fork** the repository
2. Create a new branch

   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes
4. Push your branch
5. Open a **Pull Request** with a clear description of the changes

### Contribution Guidelines

* Follow the existing coding style and project structure
* Write clear commit messages
* Ensure all features work locally before submitting
* Be respectful and constructive in discussions

---
