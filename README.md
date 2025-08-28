import { defineConfig } from "astro/config";
import mdx from "@astrojs/mdx";
import sitemap from "@astrojs/sitemap";
import cloudflare from "@astrojs/cloudflare";

export default defineConfig({
  site: "https://eae82430.sourcefiles.pages.dev",
  integrations: [mdx(), sitemap()],
  adapter: cloudflare({
    mode: "directory",
    platformProxy: {
      enabled: true,
    },
  }),
  output: "static",
});
